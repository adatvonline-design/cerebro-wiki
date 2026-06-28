---
title: "daftapp"
type: negocio
negocio: daftapp
tags: [app, acordes, github-pages, email-marketing, analitica]
created: 2026-06-27
updated: 2026-06-27
estado: activo
---

# daftapp
_Web app de progresiones de acordes. Hospedada en GitHub Pages. URL: https://adatvonline-design.github.io/daftapp/_

## Qué es

Herramienta web estilo "That Folder" para explorar y generar progresiones de acordes. Producto de Ernesto — distribuido como app gratuita, posiblemente como lead magnet o producto independiente.

## Estado actual

### Email de lanzamiento (Email #1)
- Lista: 863 contactos (misma lista que educación musical)
- Apertura: **50.22%** (excelente)
- CTR: **1.29%** (bajo)
  - Causa 1: links de texto plano en vez de botón CTA visual
  - Causa 2: dos CTAs compitiendo (video + app) → dilución de atención

### Analítica
> ⚠️ Pendiente: Sin analítica instalada. El 0% de conversión reportado en Brevo refleja falta de tracking, no uso real cero. Instalar Google Analytics o Plausible.

## Analítica — Recomendación

Sin analítica instalada, el 0% de conversión en Brevo refleja falta de tracking, no uso real cero.

### Opción recomendada: Plausible Analytics

| Criterio | Plausible | Google Analytics 4 |
|---|---|---|
| Setup | 1 línea de script en `<head>` | Script + configuración de cuenta |
| Cookie banner | No necesario (privacy-first) | Sí, requerido por GDPR/LGPD |
| Compatibilidad GitHub Pages | Total | Total |
| Costo | $9 USD/mes (hasta 10k vistas) | Gratis |
| Dashboard | Simple, limpio | Complejo |

**Por qué Plausible:** GitHub Pages es un sitio estático sin backend. Plausible no requiere cookies, no necesita banner de consentimiento, y el dashboard muestra exactamente lo que importa: páginas vistas, usuarios únicos, fuente del tráfico.

**Alternativa gratis:** Cloudflare Web Analytics — 100% gratuito, un script tag, analytics básico. Suficiente para validar si hay uso real.

**Paso de instalación (Plausible):**
```html
<!-- Agregar en <head> de index.html de daftapp -->
<script defer data-domain="adatvonline-design.github.io/daftapp" src="https://plausible.io/js/script.js"></script>
```

> ⚠️ Pendiente: Instalar Plausible (o Cloudflare Web Analytics como alternativa gratis) en daftapp. Una línea en `<head>`. Tiempo estimado: 15 min.

## Conflicto del link de bio

Resuelto con Beacons.ai — ver análisis completo en [[wiki/herramientas/calendly]].

> ⚠️ Pendiente: Resolver conflicto del link de bio de @mercadoernesto (hoy: Calendly). Decisión: usar Beacons.ai. Setup estimado: 30 min.
> ⚠️ Pendiente: Crear página propia de daftapp (posible Wix) con CTA único a la app, sin links competidores.

## Email #2

Borrador listo. Ver [[outputs/email-2-clase-diagnostica]].

> ⚠️ Pendiente: Email #2 a los 283 que abrieron — borrador en outputs/email-2-clase-diagnostica.md. Revisar y enviar desde Brevo.

## Pendientes activos

## Plan de distribución

- Página propia (posible Wix) con CTA único → app
- Sin link competidor en la misma página
- Video en Instagram con CTA a la app (en conflicto con link de bio ocupado por Calendly)

## Conexiones
- [[wiki/canales/email-brevo]] — campaña de email a 863 contactos
- [[wiki/negocios/educacion-musical]] — conflicto de link de bio
- [[wiki/conceptos/principio-conversion]] — diagnóstico: problema es conversión, no apertura
