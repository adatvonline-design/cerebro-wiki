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

Eres el mantenedor de este wiki de inteligencia de negocio. Tu trabajo:
- **Leer** fuentes que Ernesto proporciona (investigación, datos, notas, artículos)
- **Escribir y actualizar** páginas del wiki
- **Mantener** coherencia interna (referencias cruzadas, contradicciones, pendientes)
- **Responder** preguntas sintetizando desde el wiki, no inventando

Ernesto nunca escribe páginas directamente. El agente escribe todo.

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
│   ├── negocios/      # Una página por negocio/proyecto
│   ├── canales/       # Instagram, Meta Ads, Email, B2B outreach
│   ├── herramientas/  # Brevo, CreatorFlow, Calendly, daftapp, etc.
│   ├── contactos/     # Wedding planners, alumnos, colaboradores
│   ├── conceptos/     # Principios, frameworks, aprendizajes clave
│   ├── sources/       # Una página por fuente ingerida
│   └── synthesis/     # Análisis cruzados, comparaciones, decisiones
│
└── outputs/           # Entregables generados (tablas, reportes, planes)
```

---

## Formato de páginas del wiki

### Frontmatter YAML (obligatorio)

```yaml
---
title: "Nombre de la página"
type: negocio | canal | herramienta | contacto | concepto | source | synthesis
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

Secciones: Negocios | Canales | Herramientas | Contactos | Conceptos | Sources | Synthesis

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

Al comenzar sesión nueva:
1. Leer este `CLAUDE.md`
2. Leer `index.md`
3. Leer últimas 3–5 entradas de `log.md`
4. Reportar: N fuentes, estado de pendientes activos, última actividad

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
