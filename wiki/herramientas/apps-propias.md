---
title: "Apps propias"
type: herramienta
negocio: todos
tags: [apps, github-pages, desarrollo, herramientas-propias]
created: 2026-06-29
updated: 2026-06-29
---

# Apps propias
_Herramientas digitales construidas por Ernesto. Todas desplegadas en GitHub Pages bajo la cuenta `adatvonline-design`._

## Estudio Rítmico (App-rasgueos)

- **URL**: `adatvonline-design.github.io/App-rasgueos/`
- App de práctica de ritmo/rasgueo: editor de flechas arriba/abajo, metrónomo con pre-conteo de 4 clicks (Web Audio API, sin drift), modo rasgueo con snare, guardar/cargar configuración, exportar como imagen.
- Dos niveles pedagógicos: básico y funk.
- **Protección con contraseña**: evaluada y descartada — en GitHub Pages el código es visible en el navegador, así que es solo una barrera psicológica. Si se insiste: comparar hash SHA-256 en vez de texto plano.

## daftapp

- **URL**: `adatvonline-design.github.io/daftapp/`
- Generador de progresiones de acordes.
- Ver [[wiki/negocios/daftapp]] para estado, distribución y analítica pendiente.

## Calculadora de cotizaciones (giras EMQ/Páramo)

App HTML/JS para cotizar tocadas foráneas.

**Lógica de cotización:**
- Pago base por músico
- Recargo foráneo editable (default $3,000 MXN/músico)
- Viáticos por evento ($500/persona, no por día)
- Comisiones (planner y logística, sobre costo total antes de margen)
- Margen de contingencias (5–10%)
- Transporte: avión, camión, renta desde GDL (renta+gasolina+casetas), van local

Salida en **español e inglés** + "reporte interno" con desglose.

**Integración con contrato**: botón "Copiar datos para contrato" → bloque de texto estructurado para regenerar el contrato en Claude.

**Historial**: Google Sheet **"Historial Cotizaciones EMQ v2"** (Drive ID: `1KEVOIJm7kHZRKjZvgG6lv1Pmcem0nThqlKG6Sv-eg6s`).

## Curso de Armonía Moderna (lead magnet)

PDF de teoría de armonía moderna en rediseño como lead magnet premium. Trigger: comentario de keyword en Instagram → DM automático con el PDF.

## Dictado por voz (FasterWhisper)

Sistema local de dictado por voz en Windows 11. Flujo: mantener F9 graba → soltar transcribe → texto insertado donde esté el cursor.

- **Pila**: Python, faster-whisper, sounddevice, numpy, pyperclip, keyboard, Pillow, scipy
- **Alternativa más simple evaluada**: Buzz (interfaz gráfica sobre FasterWhisper)

## Conexiones

- [[wiki/negocios/daftapp]] — estado de distribución y analítica de la app
- [[wiki/negocios/emq]] — calculadora de cotizaciones para giras EMQ
- [[wiki/negocios/bruselas-live-music]] — calculadora de cotizaciones para Páramo
- [[wiki/contratos/contrato-paramo]] — contrato generado con datos de la calculadora
