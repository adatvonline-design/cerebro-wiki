---
title: "Cadena de audio — EMQ Studio"
type: herramienta
negocio: emq
tags: [audio, grabacion, preamp, interfaz, emq-studio]
created: 2026-06-29
updated: 2026-06-29
---

# Cadena de audio — EMQ Studio
_Equipamiento de grabación y procesamiento de señal de EMQ Studio._

## Equipo actual

| Equipo | Detalle |
|---|---|
| Interfaz principal | **Audient iD14 MkII** — bus-powered exclusivamente por USB (sin entrada de corriente propia) |
| Preamp/EQ | **Warm Audio WA73-EQ** (estilo Neve 1073, canal único). Entradas: XLR frontal MIC, jack 1/4" INSTRUMENT/Hi-Z, XLR trasero LINE |
| Compresor | **Empirical Labs Distressor EL8** (versión estándar, NO la EL8X). Controles: HP, Dist 2 (2do armónico/calidez), Dist 3 (3er armónico/presencia). Dist 2+3 juntos ≈ "British Mode" de la EL8X |
| Acondicionador | Furman M-80x |
| Micrófono | Pencil condenser pequeño diafragma (referido como "CV5" — confirmar modelo exacto) |

## Cadena típica de voz

```
Micrófono → WA73-EQ (Mic In) → Distressor EL8 → iD14 entrada de línea TRASERA (TRS) → DAW
```

> ⚠️ Evitar el preamp frontal del iD14 cuando se usa esta cadena — doble ganancia no deseada.

## Instrumentos y pedalería

- **Epiphone Sheraton II** (semihollow)
- **Line 6 POD Go** — salida XLR directa al PA (sin mic de gabinete). Snapshots: limpio / limpio+mod / drive / lead
- **Boss RC-500** — looper 2 pistas (Track 1 base, Track 2 melodía/solo)

## Interfaz en evaluación: Apollo Twin X

La MSI Z590-A PRO no tiene Thunderbolt nativo. Ver [[wiki/conceptos/compatibilidad-thunderbolt]] para las dos rutas que sí funcionan (MSI ThunderboltM4 8K o Gigabyte GC-Titan Ridge 2.0 en modo hack).

> ⚠️ Pendiente: Sin decisión de compra confirmada para el Apollo Twin X.
> ⚠️ Pendiente: Evaluar si conviene Apollo Twin X Thunderbolt (requiere add-on) vs. versión USB (conecta directo).

## Grabación en vivo / field recording

- Cámara de referencia en rider: Sony ZV-E10 + Sigma 30mm f/1.4
- **Grabadora recomendada para conciertos**: **Zoom H4n Pro** (cápsulas X-Y, 2 XLR, piso -120 dBu)
  - Descartado H2: pierde calidad en entornos ruidosos
  - H6 solo si hay señal de consola (4 XLR/TRS combo)

## Problema de ruido eléctrico

> ⚠️ El UPS CyberPower (onda sinusoidal simulada) genera ruido que viaja por el rail USB 5V hasta el iD14. Ver estado actualizado en [[wiki/conceptos/diagnostico-ruido-electrico]] y [[wiki/problemas-resueltos/problemas-tecnicos]].

## Conexiones

- [[wiki/negocios/emq-studio]] — espacio donde opera esta cadena
- [[wiki/conceptos/diagnostico-ruido-electrico]] — problema de zumbido 60 Hz
- [[wiki/conceptos/compatibilidad-thunderbolt]] — evaluación de Apollo Twin X
- [[wiki/herramientas/equipo-computo]] — la PC a la que se conecta la interfaz
- [[wiki/contratos/technical-rider-emq]] — requerimientos técnicos para live
