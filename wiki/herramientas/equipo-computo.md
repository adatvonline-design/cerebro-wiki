---
title: "Equipo de cómputo"
type: herramienta
negocio: todos
tags: [hardware, pc, laptop, windows]
created: 2026-06-29
updated: 2026-06-29
---

# Equipo de cómputo
_PC de escritorio (EMQ Studio) y laptop (móvil). Ambas en Windows 11._

## PC de escritorio — EMQ Studio

| Componente | Especificación |
|---|---|
| Placa madre | MSI Z590-A PRO (sin Thunderbolt nativo; header JTBT1 de 16 pines propietario MSI) |
| CPU | Intel Core i7-11700K. PL1 125W / PL2 180W / Current Limit 140A en BIOS (antes "unlimited" → 93°C) |
| RAM | 32 GB Kingston DDR4-2933 (XMP Profile 1 activado — antes corría a 2400 MHz) |
| Almacenamiento principal | WD Black SN850X NVMe |
| Almacenamiento retirado | WDC WD20EARX (608 sectores pendientes) y ST2000LM007 (8 sectores reasignados) — SMART en mal estado, **dados de baja**, ≈700 GB respaldados vía Robocopy |
| Cooler | Scythe Fuma 2 (doble torre, 2× 120mm PWM). Ruido mecánico por balero — lubricar con aceite 3 en 1 o reemplazar (Arctic P12 PWM / Noctua NF-F12 PWM) |
| SO | Windows 11 Pro, build 26200 (25H2) |
| Usuario | `nanma` |
| UPS | CyberPower 1000VA, onda sinusoidal simulada — **fuente confirmada de ruido eléctrico en la cadena de audio**. Ver [[wiki/conceptos/diagnostico-ruido-electrico]] |

### Respaldo de sistema

Imagen completa del disco C con **Macrium Reflect Free v8** (descargado vía TechSpot) a disco externo **ADATA HV620S 1TB** (NTFS, 4096 bytes, etiquetado "Imagen C"). Incluye USB de rescate booteable para restauración bare-metal.

## Laptop — Dell Latitude 5420

- **CPU**: Intel Core i5-1145G7
- **Batería**: degradada a **52%** de capacidad original (33,075 mWh de 63,000 mWh de diseño)
- Corre caliente con uso ligero; 62% de RAM en reposo (Chrome + WhatsApp)
- Recomendado: Dell Power Manager (limitar carga a 80%), limpieza + pasta térmica, reemplazo eventual de batería

## Periféricos

- **Kensington Expert Mouse** (trackball) — problema de congelación resuelto. Ver [[wiki/problemas-resueltos/problemas-tecnicos]]
- **Tablet Huion** + Krita — problema de presión de lápiz sin resolver (falta modelo exacto del Huion)

## Pendientes

> ⚠️ Pendiente: Reemplazar ventiladores del cooler Scythe Fuma 2 (Arctic P12 PWM o Noctua NF-F12 PWM).
> ⚠️ Pendiente: Confirmar modelo exacto de la tablet Huion para resolver presión de lápiz en Krita.
> ⚠️ Pendiente: Reemplazar batería del Dell Latitude 5420 eventualmente.

## Conexiones

- [[wiki/conceptos/diagnostico-ruido-electrico]] — el UPS de esta PC es la fuente del ruido en la cadena de audio
- [[wiki/conceptos/compatibilidad-thunderbolt]] — la MSI Z590-A PRO no tiene Thunderbolt nativo
- [[wiki/herramientas/cadena-audio]] — interfaz de audio conectada a esta PC
- [[wiki/problemas-resueltos/problemas-tecnicos]] — historial de problemas resueltos
