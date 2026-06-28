---
type: musica
tags: [musica, google-keep]
---


import sounddevice as sd
import numpy as np
import keyboard
import pyperclip
import time
import threading
import winsound
import tkinter as tk
import math
from faster_whisper import WhisperModel

# --- CONFIGURACIÓN TÉCNICA ---
# El modelo 'medium' ofrece un gran equilibrio entre velocidad y precisión en español
MODEL_SIZE = "medium"
model = WhisperModel(MODEL_SIZE, device="cpu", compute_type="int8")

DEVICE = 77      # ID para Audient iD14 (WASAPI)
CHANNELS = 2     # Input 2 es el canal derecho (index 1)
WHISPER_RATE = 16000
NATIVE_RATE = 48000

recording = []
is_recording = False

# --- INTERFAZ VISUAL: BOTÓN DE CONSOLA PROFESIONAL ---
class EliteIndicator:
    def __init__(self):
        self.root = tk.Tk()
        self.root.overrideredirect(True)
        self.root.attributes("-topmost", True)
        self.root.attributes("-transparentcolor", "black")
        self.root.geometry("90x90+60+60")
        self.root.configure(bg='black')

        self.offset_x = 0
        self.offset_y = 0
        self._pulse_job = None
        self._pulse_phase = 0

        self.canvas = tk.Canvas(self.root, width=90, height=90,
                                bg='black', highlightthickness=0)
        self.canvas.pack()

        self._build_chrome_ring()
        self._build_led()

        self.canvas.bind("<Button-1>", self.start_move)
        self.canvas.bind("<B1-Motion>", self.do_move)

    def _build_chrome_ring(self):
        # Sombra exterior (profundidad)
        self.canvas.create_oval(4, 6, 88, 90, fill="#_050505 outline="")
        # Cuerpo del anillo cromado
        self.canvas.create_oval(3, 3, 87, 87, fill="#_2a2a2a outline="")
        self.canvas.create_oval(5, 5, 85, 85, fill="#_383838 outline="")

        # Reflejos del cromo (Highlights)
        self.canvas.create_arc(5, 5, 85, 85, start=40, extent=175,
                               outline="#_888888 width=3, style=tk.ARC)
        self.canvas.create_arc(7, 7, 83, 83, start=50, extent=140,
                               outline="#aaaaaa width=2, style=tk.ARC)
        
        # Sombra del cromo
        self.canvas.create_arc(5, 5, 85, 85, start=220, extent=175,
                               outline="#_111111 width=3, style=tk.ARC)

        # Bisel interior (Cavidad)
        self.canvas.create_oval(17, 17, 73, 73, fill="#_0d0d0d outline="")
        self.canvas.create_oval(20, 20, 70, 70, fill="#_060606 outline="")

    def _build_led(self):
        # Capas de glow (de afuera hacia adentro)
        self.glow4 = self.canvas.create_oval(21, 21, 69, 69, fill="#_060606 outline="")
        self.glow3 = self.canvas.create_oval(26, 26, 64, 64, fill="#_080808 outline="")
        self.glow2 = self.canvas.create_oval(31, 31, 59, 59, fill="#_0a0a0a outline="")
        self.glow1 = self.canvas.create_oval(36, 36, 54, 54, fill="#_0d0d0d outline="")
        self.core  = self.canvas.create_oval(40, 40, 50, 50, fill="#_111111 outline="")

        # Reflejo especular (Efecto lente de vidrio)
        self.canvas.create_oval(29, 25, 37, 31, fill="#ffffff outline="", stipple="gray25")

    def start_move(self, event):
        self.offset_x = event.x
        self.offset_y = event.y

    def do_move(self, event):
        x = self.root.winfo_x() + event.x - self.offset_x
        y = self.root.winfo_y() + event.y - self.offset_y
        self.root.geometry(f"+{x}+{y}")

    def _stop_pulse(self):
        if self._pulse_job:
            self.root.after_cancel(self._pulse_job)
            self._pulse_job = None

    def _lerp_hex(self, c1, c2, t):
        r1,g1,b1 = int(c1[1:3],16), int(c1[3:5],16), int(c1[5:7],16)
        r2,g2,b2 = int(c2[1:3],16), int(c2[3:5],16), int(c2[5:7],16)
        return f"#{intr1r2-r1t02x}{intg1g2-g1t02x}{intb1b2-b1t02x}

    def _pulse(self, colors, speed):
        self._pulse_phase += 0.10
        t = (math.sin(self._pulse_phase) + 1) / 2
        self.canvas.itemconfig(self.core,  fill=self._lerp_hex(colors[0][0], colors[0][1], t))
        self.canvas.itemconfig(self.glow1, fill=self._lerp_hex(colors[1][0], colors[1][1], t))
        self.canvas.itemconfig(self.glow2, fill=self._lerp_hex(colors[2][0], colors[2][1], t))
        self.canvas.itemconfig(self.glow3, fill=self._lerp_hex(colors[3][0], colors[3][1], t))
        self.canvas.itemconfig(self.glow4, fill=self._lerp_hex(colors[4][0], colors[4][1], t))
        self._pulse_job = self.root.after(speed, lambda: self._pulse(colors, speed))

    def update_ui(self, state):
        self._stop_pulse()
        self._pulse_phase = 0
        if state == "off":
            for i, c in enumerate(["#_111111 "#_0d0d0d "#_0a0a0a "#_080808 "#_060606]
                self.canvas.itemconfig([self.core, self.glow1, self.glow2, self.glow3, self.glow4][i], fill=c)
        elif state == "recording":
            self._pulse([("#aa0000 "#ff3333 ("#_660000 "#cc0000 ("#_330000 "#_880000 ("#_1a0000 "#_440000 ("#_0d0000 "#_220000] 30)
        elif state == "processing":
            self._pulse([("#_005599 "#_33aaff ("#_003366 "#_0077cc ("#_001a33 "#_004488 ("#_000d1a "#_002244 ("#_000509 "#_001122] 20)

indicator = EliteIndicator()

# --- LÓGICA DE CONTROL ---
def notify_state(state):
    indicator.root.after(0, lambda: indicator.update_ui(state))

def play_audio_feedback(type):
    f = 1500 if type == "start" else 1000
    winsound.Beep(f, 80)

def callback(indata, frames, time_info, status):
    if is_recording:
        recording.append(indata[:, 1].copy()) # Input 2 de la Audient

def resample(audio, orig_rate, target_rate):
    ratio = target_rate / orig_rate
    target_len = int(len(audio) * ratio)
    return np.interp(np.linspace(0, len(audio)-1, target_len), np.arange(len(audio)), audio).astype(np.float32)

def dictation_thread():
    global is_recording, recording
    with sd.InputStream(samplerate=NATIVE_RATE, channels=CHANNELS, callback=callback, device=DEVICE):
        while True:
            keyboard.wait("F9")
            play_audio_feedback("start")
            notify_state("recording")
            is_recording, recording = True, []
            
            while keyboard.is_pressed("F9"):
                time.sleep(0.01)
            
            is_recording = False
            notify_state("processing")
            play_audio_feedback("stop")
            
            if not recording:
                notify_state("off")
                continue
            
            audio = np.concatenate(recording, axis=0).astype(np.float32)
            if np.max(np.abs(audio)) > 0: audio /= np.max(np.abs(audio))

            audio_res = resample(audio, NATIVE_RATE, WHISPER_RATE)
            segments, _ = model.transcribe(audio_res, language="es", vad_filter=True, initial_prompt="Dictado profesional.")
            text = "".join([s.text for s in segments]).strip()
            
            blacklist = ["Amara.org", "SUSCRÍBETE", "ver el vídeo", "Subtítulos por"]
            if text and not any(bad in text for bad in blacklist):
                pyperclip.copy(text)
                keyboard.write(text)
            
            notify_state("off")

threading.Thread(target=dictation_thread, daemon=True).start()
indicator.root.mainloop()