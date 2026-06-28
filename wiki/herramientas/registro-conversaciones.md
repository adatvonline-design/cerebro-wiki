---
title: "Registro de Conversaciones"
type: herramienta
negocio: todos
tags: [medicion, conversaciones, dm, whatsapp, cierre, embudo]
created: 2026-06-28
updated: 2026-06-28
---

# Registro de Conversaciones
_Sistema simple para medir DMs, WhatsApp y contactos en todos los canales. Sin este registro, las hipótesis sobre objeciones y tasas de cierre son intuiciones._

## Por qué existe esta página

El pendiente más repetido en el wiki. Sin datos de conversaciones no es posible saber:
- Cuántos prospectos llegan vs. cuántos cierran
- En qué punto se pierden (ghosting post-DM, post-Calendly, post-clase diagnóstica)
- Si la objeción real es precio, timing, confianza, u otra cosa
- Si el outreach B2B de Bruselas está generando reuniones o desapareciendo en el aire

## Cómo funciona

Ernesto reporta al agente (Claude) cualquier conversación relevante. El agente la agrega a la tabla de abajo. No requiere que Ernesto escriba en el wiki directamente.

**Mínimo a reportar por conversación:**
1. Fecha aproximada
2. Canal (dónde ocurrió)
3. Negocio (clases, Bruselas, daftapp, B2B)
4. Nombre o descripción del prospecto (puede ser anónimo: "adulta 30s Instagram")
5. Estado: En conversación / Agendó / Cerró / Ghosting / No interesado
6. Valor si cerró (MXN)
7. Nota breve si hay algo relevante (objeción mencionada, fricción, etc.)

## Tabla de conversaciones

| Fecha | Canal | Negocio | Prospecto | Estado | Valor MXN | Nota |
|---|---|---|---|---|---|---|
| — | — | — | — | — | — | _Primer registro pendiente_ |

## Estados del embudo

| Estado | Significado |
|---|---|
| **En conversación** | Respondió, hay intercambio activo |
| **Agendó** | Puso fecha en Calendly o acordaron reunión |
| **Cerró** | Pagó o firmó |
| **Ghosting** | Dejó de responder sin razón |
| **No interesado** | Dijo explícitamente que no |

## Canales que cubre

- **DM Instagram** (@mercadoernesto y @bruselaslivemusic)
- **WhatsApp** (clases y Bruselas)
- **Email directo** (respuestas a campañas)
- **B2B presencial o teléfono** (wedding planners)

## Métricas a calcular cada mes

Una vez que haya suficientes datos (mínimo 10 conversaciones):

| Métrica | Fórmula |
|---|---|
| Tasa de respuesta | Respondieron / Total contactados |
| Tasa de agenda | Agendaron / Respondieron |
| Tasa de cierre | Cerraron / Agendaron |
| Ticket promedio | Suma valores / Cierres |
| Canal más efectivo | Cierres por canal |

## Pendientes

> ⚠️ Pendiente: Iniciar registro — Ernesto debe reportar la próxima conversación para arrancar la tabla.
> ⚠️ Pendiente: Después de 10 conversaciones, calcular las métricas del embudo por primera vez.

## Conexiones

- [[wiki/canales/b2b-outreach]] — el agujero negro más urgente de medir
- [[wiki/conceptos/objeciones-clases]] — hipótesis sin confirmar hasta tener datos
- [[wiki/canales/email-brevo]] — conversaciones que vienen de Email #2
- [[wiki/herramientas/creatorflow]] — DMs automáticos que luego requieren Msg2 manual
- [[wiki/negocios/bruselas-live-music]] — outreach de bodas sin medición
