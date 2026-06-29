---
title: "STORM Research"
type: herramienta
negocio: todos
tags: [investigacion, agentes, decision, estrategia, ia]
created: 2026-06-29
updated: 2026-06-29
---

# STORM Research
_Herramienta de investigación multi-perspectiva. Basada en método Stanford STORM. Produce briefings HTML verificados para decisiones de negocio._

## Qué hace

Toma un tema o pregunta de negocio y lo analiza desde 5 lentes simultáneos:
1. **Práctico** — Qué funciona en la realidad del mercado mexicano de música/eventos/educación
2. **Académico** — Datos, estudios, evidencia verificable
3. **Escéptico** — Riesgos, supuestos no cuestionados, contra-argumentos
4. **Economista** — Estructura de mercado, precios, márgenes, viabilidad
5. **Estratega Digital** — Instagram, email, WhatsApp B2B, Meta Ads, posicionamiento

Output: archivo HTML autocontenido en `C:\Users\Dell\Documents\Claude\` con hallazgos rankeados por confiabilidad, mapa de contradicciones, acciones concretas, y fuentes verificadas.

## Cuándo usarlo

- Antes de tomar una decisión estratégica importante (invertir en un canal, cambiar precio, lanzar un producto)
- Para investigar un mercado o competencia a fondo
- Cuando hay incertidumbre y se necesita un análisis con múltiples ángulos

**No usar para:** operación diaria, seguimiento de planners, respuestas rápidas. STORM es para decisiones de 30 días o más de impacto.

## Cómo invocarlo

En cualquier sesión de Claude Code:

```
/storm [tema o pregunta]
```

Ejemplos reales para el negocio de Ernesto:
- `/storm ¿Cómo posicionar un dueto de música instrumental frente a DJs en bodas de Guadalajara?`
- `/storm Estrategias de captación de alumnos para clases de guitarra online en México`
- `/storm Viabilidad de lanzar un curso de armonía en Hotmart vs Udemy`
- `/storm Qué buscan los wedding planners en un proveedor de música en vivo`

## Archivo de skill

Ubicación: `C:\Users\Dell\.claude\commands\storm.md`

## Conexiones
- [[wiki/negocios/bruselas-live-music]] — decisiones de canal y posicionamiento
- [[wiki/negocios/educacion-musical]] — decisiones sobre cursos online y captación
- [[wiki/synthesis/analisis-estrategico-2026]] — contexto estratégico general
