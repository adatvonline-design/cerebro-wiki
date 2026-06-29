# Log — Cerebro Wiki (Ernesto Mercado)

Registro append-only de todas las operaciones. Nunca borrar entradas.

---

## [2026-06-28] restructure | Reorganización de carpetas
- **Acción**: Reestructuración del wiki para mayor claridad por negocio
- **Carpetas creadas**: `wiki/negocios/educacion-musical/`, `wiki/negocios/bruselas/`, `wiki/areas/ventas/`, `wiki/areas/marketing/`
- **Archivos movidos**: conceptos específicos de cada negocio → subcarpeta del negocio correspondiente; conceptos cross-proyecto → `areas/`; wedding-planners → `negocios/bruselas/`
- **Archivos actualizados**: `index.md` (rutas y estructura), `CLAUDE.md` (diagrama de carpetas y convenciones)
- **Regla nueva**: concepto de 1 negocio → `negocios/[negocio]/`; concepto de 2+ negocios → `areas/`

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

## [2026-06-29] ingest | Paquete cerebro-notas.zip — chats anteriores al 13 jun 2026

- **Fuente**: paquete de notas generado con Claude.ai a partir de historial de chats (anteriores al 13 jun 2026). Extraído de `~/Downloads/cerebro-notas.zip`.
- **Páginas creadas**:
  - [[wiki/negocios/emq-studio]] — construcción y tratamiento acústico del estudio (cotizaciones carpinteros, paredes A/C/D, paneles móviles)
  - [[wiki/negocios/nau-music-lab]] — estudio boutique de producción, servicios y tarifas
  - [[wiki/negocios/nuages]] — jazz manouche, problema de identidad en streaming, recomendación DistroKid
  - [[wiki/herramientas/equipo-computo]] — specs completos PC de escritorio (MSI Z590, i7-11700K, XMP, UPS, backups) y Dell Latitude 5420
  - [[wiki/herramientas/cadena-audio]] — iD14 MkII, WA73-EQ, Distressor EL8, POD Go, Boss RC-500, Apollo Twin X en evaluación
  - [[wiki/herramientas/camara-gimbal]] — Sony ZV-E10 + Sigma 30mm; Crane M3 dañado; DJI RS 3 Mini recomendado; Zoom H4n Pro
  - [[wiki/herramientas/apps-propias]] — Estudio Rítmico, calculadora de giras EMQ/Páramo, curso de armonía moderna (lead magnet), dictado por voz (FasterWhisper)
  - [[wiki/contratos/contrato-paramo]] — plantilla performance agreement en inglés (primera boda: Punta Mita, mayo 2026)
  - [[wiki/contratos/contrato-renta-colonias]] — renta Colonias 457, $6,700/mes, vigencia mar 2026–mar 2027, 3 cláusulas de riesgo
  - [[wiki/contratos/technical-rider-emq]] — 13 canales, 5 monitores, stage plot, hospitalidad
  - [[wiki/conceptos/aislamiento-acustico]] — masa-aire-masa, MLV, ruido de impacto, ANC, resonancias de cavidad
  - [[wiki/conceptos/diagnostico-ruido-electrico]] — caso 60 Hz: UPS onda simulada → USB → iD14. Aislador ADuM3165. Estado al 4 jun 2026
  - [[wiki/conceptos/compatibilidad-thunderbolt]] — MSI Z590-A PRO: ThunderboltM4 8K (oficial) vs. Gigabyte GC-Titan Ridge 2.0 (hack)
  - [[wiki/problemas-resueltos/problemas-tecnicos]] — tabla completa diagnóstico → solución → estado (11 problemas)
- **Páginas actualizadas**:
  - [[wiki/negocios/emq]] — roadie (+1, total 6 en gira), documentación de producción, refs a Drive (historial cotizaciones EMQ v2)
  - [[wiki/negocios/bruselas-live-music]] — nombre dual Páramo/Bruselas documentado, refs a contrato y calculadora
  - [[wiki/negocios/educacion-musical]] — 9 alumnos presenciales (mar 2026), MailerLite 2,500 contactos, Udemy activo, plataformas internacionales, pendiente alumnos angloparlantes
  - [[wiki/canales/instagram-mercadoernesto]] — análisis 12 publicaciones (mar–jun 2026), embudo 3 capas, configuración Meta Ads recomendada, exportación CSV
  - [[wiki/canales/email-brevo]] — dos listas documentadas (MailerLite 2,500 + Brevo 863), secuencia MailerLite propuesta, infraestructura Bruselas
- **Pendientes detectados**:
  - Coche: shortlist Toyota Yaris / Nissan Versa / Honda Fit / Kia Rio / Nissan Sentra (~$170k MXN). MG ZS y BYD descartados
  - Apollo Twin X: decidir entre Thunderbolt (con add-on) vs. versión USB
  - Aislador USB ADuM3165: compra pendiente (pero el diagnóstico de ruido puede haber cambiado)
  - Gimbal DJI RS 3 Mini: compra pendiente
  - DistroKid para Nuages: migración pendiente
  - Aclarar fórmula de luz en contrato de renta Colonias 457
- **NO ingresado**: carpeta `personal/` del zip — ver abajo para decisión pendiente
- **Nota de alcance**: todo el paquete viene de chats anteriores al 13 jun 2026. Al menos el diagnóstico del ruido eléctrico cambió en sesión posterior ("ruido USB" → "ground loop analógico"). Verificar antes de actuar sobre la tabla de problemas.

## [2026-06-29] ingest | Actualización ruido eléctrico — hub USB instalado

- **Fuente**: confirmación directa de Ernesto
- **Dato nuevo**: el hub USB redujo el ruido pero no lo eliminó → confirma dos fuentes simultáneas: (1) componente USB parcialmente resuelta por el hub, (2) ground loop analógico en la cadena XLR/línea aún sin resolver
- **Páginas actualizadas**:
  - [[wiki/conceptos/diagnostico-ruido-electrico]] — resultado real del hub, hipótesis de dos fuentes, próximos pasos para aislar el componente analógico
  - [[wiki/problemas-resueltos/problemas-tecnicos]] — estado actualizado a "parcialmente resuelto"

## [2026-06-29] decisión | personal/ — pendiente de confirmación del usuario

- **Contenido**: datos de identificación, salud (composición corporal, suplementos, consultas médicas) y relación de pareja
- **Estado**: NO subida al repo. El usuario debe decidir: (a) excluir del repo, (b) agregar a `.gitignore` local, o (c) rama separada sin push a GitHub

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
