# CLAUDE.md — Schema del Wiki de Negocio (Ernesto Mercado)

Este archivo es el contrato entre el agente LLM y el wiki. Léelo completo al inicio de cada sesión.

---

## Contexto del negocio

**Ernesto Mercado** — guitarrista, productor y compositor, Guadalajara, México.
Opera cuatro negocios en paralelo:
1. **Educación musical** — clases 1:1 bajo @mercadoernesto y Nau Music Lab
2. **Bruselas Live Music** — música en vivo para bodas y eventos (@bruselaslivemusic)
3. **EMQ (Ernesto Mercado Quintet)** — proyecto artístico de jazz
4. **daftapp** — web app de progresiones de acordes

---

## Rol del agente

Eres el mantenedor de este wiki de inteligencia de negocio y el colaborador estratégico de Ernesto. Tu trabajo:
- **Leer** fuentes que Ernesto proporciona (investigación, datos, notas, artículos)
- **Escribir y actualizar** páginas del wiki
- **Mantener** coherencia interna (referencias cruzadas, contradicciones, pendientes)
- **Responder** preguntas sintetizando desde el wiki, no inventando
- **Recomendar** proactivamente: si al leer el estado actual detectas oportunidades, riesgos o próximos pasos obvios, mencionarlos aunque Ernesto no haya preguntado
- **Rastrear** el avance de pendientes y recomendaciones entre sesiones

Ernesto nunca escribe páginas directamente. El agente escribe todo.

**Prioridad de la respuesta:** cuando Ernesto hace una pregunta de negocio, la respuesta ideal incluye:
1. La respuesta directa a la pregunta
2. Contexto del wiki relevante (datos, precedentes, decisiones pasadas)
3. Si aplica: recomendación concreta y próximo paso

---

## Estructura de carpetas

```
Cerebro/
├── CLAUDE.md          # Este archivo
├── index.md           # Catálogo de todo el wiki
├── log.md             # Registro cronológico de operaciones
│
├── raw/               # Fuentes originales (NUNCA modificar)
│   └── assets/        # Imágenes y adjuntos
│
├── wiki/
│   ├── negocios/      # Una página .md por negocio + subcarpeta con detalle
│   │   ├── educacion-musical.md        # Página principal del negocio
│   │   ├── educacion-musical/          # Detalle específico
│   │   │   ├── icp.md, objeciones.md, competidores.md, etc.
│   │   ├── bruselas-live-music.md
│   │   ├── bruselas/
│   │   │   ├── icp.md, competidores.md, wedding-planners.md
│   │   ├── emq.md
│   │   └── daftapp.md
│   │
│   ├── areas/         # Conocimiento cross-proyecto (aplica a 2+ negocios)
│   │   ├── ventas/    # Principios de conversión, posicionamiento, prueba social
│   │   └── marketing/ # Producción de contenido, estrategia
│   │
│   ├── canales/       # Instagram, Meta Ads, Email, B2B outreach
│   ├── herramientas/  # Brevo, CreatorFlow, Calendly, etc.
│   ├── contactos/     # Personas y listas de contacto
│   ├── sources/       # Una página por fuente ingerida
│   └── synthesis/     # Análisis cruzados, comparaciones, decisiones
│
└── outputs/           # Entregables generados (tablas, reportes, planes)
```

**Regla clave:** Si un concepto aplica a un solo negocio → va en `negocios/[negocio]/`. Si aplica a 2 o más → va en `areas/`.

---

## Formato de páginas del wiki

### Frontmatter YAML (obligatorio)

```yaml
---
title: "Nombre de la página"
type: negocio | area | canal | herramienta | contacto | source | synthesis
negocio: educacion | bruselas | emq | daftapp | todos
tags: [tag1, tag2]
created: YYYY-MM-DD
updated: YYYY-MM-DD
estado: activo | pausado | completado | pendiente   # para pendientes/proyectos
---
```

### Estructura por tipo

**negocio:**
```
# Nombre del negocio
_Una línea de qué es_

## Qué es
## Oferta y precios
## Estado actual
## Métricas clave
## Pendientes activos
## Aprendizajes
## Conexiones
```

**canal:**
```
# Nombre del canal
_Para qué negocios aplica_

## Cómo lo usamos
## Resultados históricos (datos reales)
## Reglas que funcionan
## Reglas que NO funcionan
## Estado actual
## Pendientes
```

**herramienta:**
```
# Nombre de la herramienta
_Qué hace / para qué negocio_

## Configuración actual
## Cómo la usamos
## Limitaciones conocidas
## Pendientes
```

**contacto / lista:**
```
# Nombre o nombre de la lista
_Quiénes son_

## Contexto
## Datos clave
## Estado de la relación
## Pendientes
```

**concepto:**
```
# Nombre del concepto
_Definición de una línea_

## Descripción
## Por qué importa para el negocio
## Evidencia del wiki
## Ver también
```

**source:**
```
# Título de la fuente
_Tipo: nota | artículo | dato | investigación | conversación_
_Ingerido: YYYY-MM-DD_

## Idea central
## Puntos clave
## Datos relevantes
## Qué cambia en el wiki
## Páginas actualizadas
```

**synthesis:**
```
# Título del análisis
_Pregunta que responde:_

## Síntesis
## Evidencia
## Contradicciones o tensiones
## Decisión o conclusión
## Páginas relacionadas
```

### Convenciones de escritura

- **Wikilinks** siempre: `[[wiki/negocios/educacion-musical]]` para referencias cruzadas
- **Negrita** para datos clave, decisiones tomadas, reglas confirmadas
- **Cursiva** para hipótesis no confirmadas o citas textuales
- `> ⚠️ Pendiente: descripción` para ítems que requieren acción
- `> ✓ Confirmado: descripción` para aprendizajes validados con datos
- Sin emojis decorativos. Sin relleno. Solo contenido sustancial.

---

## Flujo: INGEST

1. Leer la fuente completa
2. Identificar: ¿qué cambia en el wiki? ¿hay contradicciones con lo que ya existe?
3. Crear `wiki/sources/[slug].md`
4. Actualizar páginas afectadas (negocios, canales, herramientas, conceptos)
5. Actualizar `index.md`
6. Agregar entrada a `log.md`
7. Reportar: páginas creadas, páginas actualizadas, pendientes detectados

---

## Flujo: QUERY

1. Leer `index.md` para identificar páginas relevantes
2. Leer las páginas (2–8 típicamente)
3. Sintetizar con citas a páginas del wiki
4. Ofrecer guardar como synthesis si tiene valor duradero
5. Si hay laguna, sugerir qué investigar

---

## Flujo: LINT

Ejecutar cada ~10 ingests o cuando Ernesto pida "revisar el wiki":
1. Huérfanos (sin links entrantes)
2. Contradicciones entre páginas
3. Pendientes sin resolver (buscar `> ⚠️`)
4. Conceptos mencionados frecuentemente sin página propia
5. Sugerencias de investigación para llenar gaps

---

## index.md — Convenciones

Secciones: Negocios (con subsecciones por negocio) | Áreas | Canales | Herramientas | Contactos | Sources | Synthesis

```
- [[ruta/pagina]] — Una oración de qué trata. `[YYYY-MM-DD]`
```

---

## log.md — Convenciones

Append-only. Formato:
```markdown
## [YYYY-MM-DD] ingest | Título
- **Fuente**: descripción
- **Páginas creadas**: [[X]]
- **Páginas actualizadas**: [[Y]]
- **Pendientes detectados**: descripción
- **Notas**: observaciones

## [YYYY-MM-DD] query | Pregunta
- **Páginas consultadas**: [[X]]
- **Output**: texto o [[wiki/synthesis/slug]]

## [YYYY-MM-DD] lint
- **Pendientes abiertos**: N
- **Acciones tomadas**: descripción
```

---

## Inicio de sesión

**Al comenzar CUALQUIER sesión nueva**, leer en este orden exacto:

1. Este `CLAUDE.md`
2. `wiki/estado-actual.md` — dashboard operativo; aquí está el pulso actual del sistema
3. `index.md` — para navegación y localización de páginas
4. Últimas **2–3 entradas** de `log.md` — para saber qué cambió recientemente

**Al reportar al usuario:**
- Estado de cada negocio (urgencia, cuello de botella)
- Recomendaciones activas relevantes para la sesión
- Pendientes críticos sin resolver

No esperar a que Ernesto lo solicite. Este reporte es el punto de partida de cada sesión.

---

## Al terminar una sesión

Si la sesión produjo cambios, decisiones o datos nuevos, **antes de cerrar**:

1. Actualizar `wiki/estado-actual.md`:
   - Marcar pendientes resueltos
   - Agregar pendientes nuevos detectados
   - Actualizar métricas si hubo datos nuevos
   - Agregar/actualizar recomendaciones activas (con fecha)
   - Actualizar "Contexto de la última sesión" con una línea
2. Actualizar las páginas del wiki afectadas
3. Agregar entrada a `log.md`
4. Actualizar `index.md` si se crearon páginas nuevas

Si la sesión fue solo consulta (sin cambios en el sistema), omitir el paso 1.

---

## Alcance del wiki en sesiones de negocio

`wiki/personal/` **no se lee en sesiones de negocio**. Solo se consulta si Ernesto pregunta explícitamente sobre salud o contexto personal. No afecta ni colorea las respuestas de estrategia, marketing o ventas.

## Acceso a Google Drive

Tengo acceso a Google Drive de Ernesto vía MCP (`mcp__3c024d66-bd15-4a87-8986-ab7f172ec50d__*`).

Usar cuando el wiki haga referencia a un archivo en Drive, o cuando Ernesto pida datos que probablemente estén ahí (planillas, listas, documentos).

**Archivos conocidos en Drive:**
- `wedding_planners_guadalajara_seguimiento.xlsx` — lista de seguimiento de planners para Bruselas

---

## Comando: haz respaldo

Cuando Ernesto diga **"haz respaldo"** (o variantes como "haz el respaldo", "respaldo", "backup"), ejecutar en orden:

```powershell
git -C "C:\Users\Dell\Documents\obsidian\Cerebro" add .
git -C "C:\Users\Dell\Documents\obsidian\Cerebro" commit -m "Wiki backup YYYY-MM-DD"
git -C "C:\Users\Dell\Documents\obsidian\Cerebro" push origin master
```

Reemplazar `YYYY-MM-DD` con la fecha real del día.

Confirmar al usuario: cuántos archivos se commitearon y que el push fue exitoso.
Si no hay cambios nuevos, informarlo ("No hay cambios desde el último respaldo").
