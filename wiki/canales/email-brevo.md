---
title: "Email Marketing — Brevo"
type: canal
negocio: todos
tags: [email, brevo, lista, campana, apertura, ctr]
created: 2026-06-27
updated: 2026-06-29
---

# Email Marketing — Brevo
_Canal de email marketing. Herramienta: Brevo (plan Starter). Lista de 863 contactos compartida entre educación musical y daftapp._

## Listas de correo (dos listas distintas)

| Lista | Plataforma | Contactos | Para qué |
|---|---|---|---|
| Lista clases/@mercadoernesto | **MailerLite** | ≈2,500 contactos | Secuencia de conversión para clases 1:1 y cursos digitales |
| Lista Brevo (limpiada) | **Brevo** | 863 contactos | Email #1 enviado; campaña fría Bruselas |

> ⚠️ Las dos listas son independientes y tienen propósitos distintos — no mezclar.

### Lista Brevo: segmento activo

- **Total**: 863 contactos (limpiada y cargada ✓)
- **Segmento activo (Email #1)**: 283 contactos que abrieron Email #1

## Campañas activas

### Email #1 — Lanzamiento (enviado)
- **Para**: lista completa (863)
- **Apertura**: 50.22% (excelente — referencia industria ~20–25%)
- **CTR**: 1.29% (bajo)
  - Causa 1: links de texto plano en vez de botón CTA visual
  - Causa 2: dos CTAs compitiendo (video daftapp + app daftapp)

### Email #2 — Clase diagnóstica gratuita (borrador listo)

- **Para:** segmento que abrió Email #1 (283 contactos)
- **Asunto:** `Te regalo 25 minutos`
- **CTA único:** botón visual → Calendly directo (no depende del link de bio)
- **Borrador completo:** [[outputs/email-2-clase-diagnostica]]

> ⚠️ Pendiente: Revisar borrador y enviar desde Brevo. El CTA va directo a Calendly — no hay conflicto con el link de bio.

### Campaña fría — Bruselas Live Music (enviada)
- **Para**: ~80 wedding planners
- **Desde**: sender `info@bruselaslivemusic.com` verificado
- **Dominio**: `bruselaslivemusic.com` (Namecheap)
- **Estado**: enviada, en seguimiento

## Aprendizajes

> ✓ Confirmado: Alta tasa de apertura (50%) con bajo CTR (1.29%) = el copy del asunto funciona, pero el contenido del email no convierte. Problema en el cuerpo: links planos y CTAs duplicados.
> ✓ Confirmado: Un solo CTA claro + botón visual es la corrección necesaria.

## Segmentación de la lista

La lista de 863 contactos fue cargada sin segmentación documentada. Pregunta abierta: ¿hay distinción entre contactos interesados en clases vs. daftapp?

> ⚠️ Pendiente: Revisar en Brevo si existen atributos o etiquetas en los 863 contactos que permitan separar interés en clases vs. daftapp. Si no existe, considerar agregar un campo de interés en el siguiente email.

## Pendientes

> ⚠️ Pendiente: Email #2 — borrador listo en [[outputs/email-2-clase-diagnostica]]. Revisar y enviar a los 283 que abrieron Email #1.
> ⚠️ Pendiente: Revisar resultados de campaña Bruselas después del 2026-06-30 (apertura, respuestas, seguimiento).
> ⚠️ Pendiente: Verificar segmentación clases vs. daftapp en la lista de 863.

## Secuencia MailerLite (lista clases — propuesta)

Secuencia de 3 emails para los ≈2,500 contactos:
1. Reactivación con valor gratuito
2. Historia personal y autoridad
3. Oferta directa con escasez de cupos

## Infraestructura Brevo (campaña Bruselas)

- Dominio: **bruselaslivemusic.com** (Namecheap)
- Sender verificado: info@bruselaslivemusic.com (DKIM/SPF configurados)
- ⚠️ No enviar campañas desde Gmail: límite de 500 destinatarios/día y peor entregabilidad
- Alternativa de email: Zoho Mail gratuito o el email incluido por Namecheap

## Conexiones
- [[wiki/negocios/educacion-musical]] — Email #2 pendiente + lista MailerLite
- [[wiki/negocios/daftapp]] — causa del CTA doble en Email #1
- [[wiki/negocios/bruselas-live-music]] — campaña fría a planners
- [[wiki/herramientas/brevo]] — configuración técnica
- [[wiki/areas/ventas/principio-conversion]] — alta apertura no es suficiente; conversión es lo que importa
