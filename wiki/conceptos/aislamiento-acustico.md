---
title: "Aislamiento acústico — principios reutilizables"
type: area
negocio: emq
tags: [acustica, aislamiento, concepto, reutilizable]
created: 2026-06-29
updated: 2026-06-29
---

# Aislamiento acústico — principios reutilizables
_Principios generales aplicados en el diseño del EMQ Studio. Válidos para cualquier proyecto de tratamiento acústico._

## Masa-aire-masa

Una cámara de aire entre dos superficies (vidrio y tapón de madera) **mejora** el aislamiento si **no** se rellena con material rígido — rellenarla acopla las dos superficies y degrada el aislamiento.

- Tratamiento correcto: sellar el perímetro con backer rod + sellador poliuretano flexible (SikaFlex)
- Si se quiere amortiguar resonancia interna: material suelto NO comprimido (lana mineral suelta dentro de la cavidad)
- **Nunca**: espuma expansiva contra el vidrio (riesgo de transmisión de presión/vibración)

## Mass Loaded Vinyl (MLV)

Funciona por **masa**, no por profundidad. Ideal cuando el espacio disponible es muy limitado (≤2.5 cm). Atenuación típica ≈26 dB. Útil para ruidos de baja/media-baja frecuencia (80–500 Hz: vehículos, perros).

## Ruido de impacto (pisadas desde piso superior)

Se trata mejor en la fuente. Si no es posible: plafón falso desacoplado con clips resilientes (Genie Clip, RSIC-1) + lana mineral en cavidad + doble capa de tablaroca con compuesto viscoelástico (Green Glue) + sellador acústico perimetral. Reducción típica: **10–15 dB**, a costa de 10–15 cm de altura de techo.

### Por qué la cancelación activa de ruido (ANC) NO sirve a escala de habitación

ANC funciona en audífonos porque la cavidad es pequeña y controlada. A escala de habitación, la cancelación es válida en un punto pero **refuerza** el ruido a media longitud de onda de distancia. El ruido de impacto es además demasiado impulsivo/banda ancha para cualquier DSP.

Excepción real parcial: trampas de graves activas (PSI Audio AVAA) por debajo de ~150 Hz. Los sistemas pasivos masa-resorte-masa son superiores en costo-efectividad.

## Resonancia de cavidades poco profundas

Una cavidad abierta de profundidad *d* tiene resonancia de cuarto de onda en **f = c / (4×d)**. Para d = 10 cm → f ≈ 858 Hz (efecto "nicho" en medios-agudos, sin resonancias graves).

Tratamiento: lana mineral de alta densidad (60–80 kg/m³) detrás de tela acústica — absorbe banda ancha >500 Hz.

## Paneles rígidos con NRC alto sobre superficies curvas

Un panel NRC ≈0.80 elimina la focalización, pero **el problema de instalarlo sobre una curva es constructivo, no acústico** — las juntas se notan. Mejor: usarlo en superficies planas adyacentes y reservar lana mineral + tela tensada para la superficie curva.

## Conexiones

- [[wiki/negocios/emq-studio]] — aplicación práctica de estos principios
