# Log — Cerebro Wiki (Ernesto Mercado)

Registro append-only de todas las operaciones. Nunca borrar entradas.

---

## [2026-06-27] setup | Inicialización del wiki
- **Acción**: Creación de la estructura base del wiki
- **Archivos creados**: `CLAUDE.md`, `index.md`, `log.md`
- **Carpetas creadas**: `raw/`, `raw/assets/`, `wiki/negocios/`, `wiki/canales/`, `wiki/herramientas/`, `wiki/contactos/`, `wiki/conceptos/`, `wiki/sources/`, `wiki/synthesis/`, `outputs/`
- **Notas**: Wiki inicializado con schema adaptado al negocio de Ernesto.

---

## [2026-06-27] ingest | Competidores Bruselas, métricas de ventas, producción de contenido
- **Fuente**: Investigación web (Jazzette, Loretta, MZ Jazz) + respuestas directas de Ernesto
- **Páginas creadas**:
  - [[wiki/conceptos/competidores-bruselas]]
  - [[wiki/conceptos/metricas-ventas-clases]]
  - [[wiki/conceptos/produccion-contenido]]
- **Páginas actualizadas**: `index.md`
- **Hallazgo clave**: nadie en GDL ocupa explícitamente el nicho Páramo/Hermanos Gutiérrez para bodas — ventana de posicionamiento abierta
- **Alerta**: Loretta cobra desde $3,700 MXN vs. $12,000–$25,000 de Bruselas — están en segmentos distintos, no compiten directamente
- **Alerta producción**: clips de YouTube reutilizados tienen riesgo de copyright en IG. Documentado con alternativas.
- **Dato crítico**: tasa histórica de cierre (1 alumno/3 meses) requiere multiplicarse 18–36x para alcanzar la meta urgente.

---

## [2026-06-27] ingest | Competidores, testimonios, ICP Bruselas, comunidad de alumnos
- **Fuente**: Investigación web (ernestomercado.com.mx, BuscaTuProfesor.mx, Superprof.mx, búsquedas) + respuestas directas de Ernesto
- **Páginas creadas**:
  - [[wiki/conceptos/competidores-clases-guitarra-gdl]]
  - [[wiki/conceptos/posicionamiento-precio]]
  - [[wiki/conceptos/testimonios-alumnos]]
  - [[wiki/conceptos/icp-bruselas]]
- **Páginas actualizadas**:
  - [[wiki/conceptos/diferenciadores-clases]] — actividades fuera de clase documentadas (café, reuniones 1–2/año)
  - `index.md`
- **Contradicciones detectadas**: discrepancia de duración de clase entre sitio web (50 min) y Calendly (60 min) — pendiente resolver
- **Pendientes detectados**: localizar Jorge Cárdenas en Superprof; segmentar planners por tipo de boda; crear contenido de nicho para Bruselas
- **Datos clave**: Mercado promedia $250/h. Ernesto cobra ~$720/h equiv. — 2.9x el mercado. Superprof bloqueó acceso directo. Jorge Cárdenas no localizado.

---

## [2026-06-27] ingest | ICP, diferenciadores y objeciones de clases
- **Fuente**: Preguntas directas a Ernesto sobre el perfil del alumno ideal
- **Páginas creadas**:
  - [[wiki/conceptos/icp-clases]]
  - [[wiki/conceptos/diferenciadores-clases]]
  - [[wiki/conceptos/objeciones-clases]]
  - [[wiki/conceptos/prueba-social]]
- **Páginas actualizadas**: `index.md`, [[wiki/sources/briefing-inicial-negocio]]
- **Contradicciones detectadas**: ninguna
- **Notas**: La objeción de precio es una hipótesis de Ernesto, no un dato confirmado. Se necesita registro de conversaciones en DM para validar.

---

## [2026-06-27] ingest | Briefing Inicial del Negocio
- **Fuente**: Conversación directa — estado completo de los 4 negocios
- **Páginas creadas**:
  - [[wiki/sources/briefing-inicial-negocio]]
  - [[wiki/negocios/educacion-musical]]
  - [[wiki/negocios/bruselas-live-music]]
  - [[wiki/negocios/emq]]
  - [[wiki/negocios/daftapp]]
  - [[wiki/canales/meta-ads]]
  - [[wiki/canales/instagram-mercadoernesto]]
  - [[wiki/canales/email-brevo]]
  - [[wiki/canales/b2b-outreach]]
  - [[wiki/herramientas/creatorflow]]
  - [[wiki/herramientas/calendly]]
  - [[wiki/herramientas/brevo]]
  - [[wiki/contactos/wedding-planners-guadalajara]]
  - [[wiki/conceptos/principio-conversion]]
- **Páginas actualizadas**: `index.md` (catálogo completo), `log.md`
- **Contradicciones detectadas**: ninguna (primer ingest)
- **Pendientes detectados**: ~15 ítems marcados con `> ⚠️` distribuidos en varias páginas
- **Notas**: Ingest fundacional. El wiki parte con una base sólida de contexto real, métricas y configuraciones actuales.

## [2026-06-28] organización | Clasificación y limpieza de notas Google Keep

- **Acción**: Clasificación automática de 1,513 notas de Google Keep con script Python por keywords
- **Distribución resultante**:
  - `Google Keep/musica/` — 352 notas (repertorios, progresiones, licks, referencias)
  - `Google Keep/negocio/` — 97 notas (clases, eventos, marketing, juntas)
  - `Google Keep/ideas/` — 21 notas (conceptos, recursos, contenido)
  - `Google Keep/herramientas/` — 1 nota (guía Sony ZV-E10 + gimbal)
  - `Google Keep/archivo/` — 1,042 notas (triviales, completadas, personales, sin clasificar)
- **Ningún archivo borrado** — solo reorganización en subcarpetas

## [2026-06-28] ingest | Notas Google Keep → wiki

- **Fuente**: Notas de negocio e ideas de Google Keep (dic. 2025 principalmente)
- **Páginas actualizadas**:
  - [[wiki/negocios/emq]] — agregada alineación completa (Eli sax, Freedy bajo, Shatter piano, Guillermo bat), descripción artística, links Spotify/YouTube/web
  - [[wiki/canales/instagram-mercadoernesto]] — agregadas métricas reales dic. 2025: "switch productor" 758k vistas/72k interacciones, "cuidados músico" 220k vistas, "tensiones" 16k vistas/299 seguidores
- **Páginas creadas**:
  - [[wiki/canales/youtube-mercadoernesto]] — canal YouTube, datos de "acordes aumentados": 8.26% CTR, 1,145 vistas en 4h, 47% retención
  - [[wiki/herramientas/obs-zoom-clases]] — setup técnico OBS+Zoom+VoiceMeeter+Ableton para clases en línea
- **Pendientes detectados**: Definir estrategia de distribución EMQ, cadencia YouTube, performance histórico del canal
- **No ingresado** (fuera de scope del wiki): listas personales, películas, regalos, gastos domésticos, mensajes personales, calendarios de disponibilidad

## [2026-06-28] ingest | Sesión de mantenimiento — 6 bloques de pendientes

- **Fuente**: Instrucciones directas de Ernesto + contexto del wiki
- **Páginas creadas**:
  - [[wiki/herramientas/registro-conversaciones]] — sistema de registro de DMs/WhatsApp para todos los canales
  - [[outputs/email-2-clase-diagnostica]] — borrador completo de Email #2 (clase diagnóstica gratuita, CTA único a Calendly)
- **Páginas actualizadas**:
  - [[wiki/herramientas/calendly]] — evaluación de alternativas al link de bio (Beacons.ai recomendado), pros/contras
  - [[wiki/negocios/daftapp]] — recomendación de analítica (Plausible / Cloudflare Web Analytics), conflicto link de bio resuelto con referencia a Beacons.ai
  - [[wiki/herramientas/creatorflow]] — pasos detallados para conectar cuenta, configurar Msg1/Msg3, y probar flujo completo
  - [[wiki/canales/email-brevo]] — referencia a borrador Email #2, nota de segmentación clases vs. daftapp
  - [[wiki/canales/b2b-outreach]] — referencia a registro-conversaciones
  - [[wiki/conceptos/objeciones-clases]] — pendiente de registro marcado como resuelto con referencia al sistema
  - [[wiki/negocios/bruselas-live-music]] — referencia a registro-conversaciones, pendiente bodas.com.mx documentado
  - [[wiki/negocios/educacion-musical]] — nota de discrepancia duración en sitio web
  - [[wiki/herramientas/obs-zoom-clases]] — pendiente de verificación de estudio detallado
  - [[wiki/conceptos/competidores-clases-guitarra-gdl]] — corregido cálculo de precio/hora (50 min → 60 min; $720/h → $600/h)
  - `index.md` — nueva herramienta agregada, totales actualizados
- **Decisiones tomadas**:
  - Link de bio: recomendación Beacons.ai (< 30 min setup, gratis, diseñado para creadores)
  - Analítica daftapp: recomendación Plausible; alternativa gratis Cloudflare Web Analytics
  - Email #2: asunto "Te regalo 25 minutos", CTA único a Calendly directo (sin conflicto con bio)
  - Duración oficial de clase: **60 min** (Calendly corregido). Sitio web muestra 50 min — necesita actualización externa
- **Pendientes detectados / confirmados**:
  - Jorge Cárdenas en Superprof: sigue sin localizar (intentado sesión anterior)
  - Reseñas bodas.com.mx: requiere verificación manual
  - Setup OBS/Zoom nuevo estudio: requiere prueba de Ernesto
  - Registro de conversaciones: primera entrada pendiente — Ernesto debe reportar próxima conversación
  - Segmentación lista 863 (clases vs. daftapp): revisar en Brevo
- **Corrección de error previo**: precio/hora de Ernesto recalculado a $600 MXN/h (no $720/h). El cálculo anterior usaba 50 min de clase en vez de 60 min.
