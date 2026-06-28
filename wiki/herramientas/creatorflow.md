---
title: "CreatorFlow"
type: herramienta
negocio: educacion
tags: [dm, automatizacion, instagram, keyword, manychat]
created: 2026-06-27
updated: 2026-06-27
---

# CreatorFlow
_Herramienta de automatización de DM en Instagram por palabra clave. Elegida sobre ManyChat y LinkDM._

## Por qué CreatorFlow

Elegida después de evaluar:
- **ManyChat**: descartada (razón no especificada en briefing)
- **LinkDM**: descartada (razón no especificada en briefing)
- **CreatorFlow**: elegida — plan gratis disponible, 500 DM/mes suficientes para el volumen actual

> ⚠️ Pendiente: Documentar por qué se descartaron ManyChat y LinkDM específicamente.

## Configuración actual (educación musical)

- **Plan**: Gratis
- **Límite**: 500 DM/mes
- **Cuenta conectada**: @mercadoernesto (pendiente conectar ✓)
- **Keyword trigger**: "CLASE"

### Flujo de DM configurado
| Mensaje | Tipo | Contenido |
|---|---|---|
| Msg1 | Automático | Info de clases ($600 individual, $2,500/5 clases, presencial y online) + pregunta de calificación (instrumento/meta del alumno) |
| Msg2 | Manual (Ernesto) | Respuesta personalizada en 24–48h |
| Msg3 | Automático | Seguimiento |

**Email gate**: explícitamente rechazado — crea fricción en el momento de mayor intención de compra.

## Pasos para activar (en orden)

### Paso 1 — Conectar cuenta
1. Entrar a [creatorflow.io](https://creatorflow.io)
2. Ir a **Accounts → Connect Instagram**
3. Autorizar @mercadoernesto con las credenciales de Meta Business Suite
4. Verificar que aparece "Connected" en el dashboard

### Paso 2 — Crear flujo keyword "CLASE"
1. Ir a **Flows → New Flow**
2. Trigger: **Comment contains** → `CLASE` (en mayúsculas, sensible a mayúsculas si la herramienta lo permite; agregar también `clase`, `Clase` si acepta múltiples)
3. **Msg1 (automático inmediato):**
   ```
   Hola [nombre]! 🎸
   
   Clases 1:1 de guitarra, armonía y composición con Ernesto Mercado.
   
   💰 $600 por clase individual | $2,500 paquete de 5 clases
   📍 Presencial (Guadalajara) u online
   
   Una pregunta rápida: ¿qué instrumento tocas y qué quieres lograr con las clases?
   ```
4. **Msg3 (automático, seguimiento si no hubo respuesta en 24h):**
   ```
   Hola [nombre], ¿te quedó alguna duda sobre las clases?
   Puedo agendar una plática de 5 min para contarte más — sin compromiso.
   ```
5. Guardar flujo

### Paso 3 — Probar antes de lanzar pauta
1. Desde una cuenta de Instagram diferente (personal u otra), comentar "CLASE" en cualquier post de @mercadoernesto
2. Verificar que llega Msg1 en DM en menos de 1 minuto
3. No responder — esperar 24h y verificar que llega Msg3
4. Si funciona: lanzar pauta

> ⚠️ Pendiente: Ejecutar Paso 1 (conectar cuenta). Requiere acceso a Meta Business Suite de @mercadoernesto.
> ⚠️ Pendiente: Ejecutar Paso 2 (configurar flujo Msg1 y Msg3 con los textos de arriba).
> ⚠️ Pendiente: Ejecutar Paso 3 (prueba completa desde segunda cuenta antes de activar pauta).

## Limitaciones conocidas

- 500 DM/mes en plan gratis — monitorear si se supera con la campaña de pauta activa
- Msg2 es manual: requiere que Ernesto responda en 24–48h; el cuello de botella es su disponibilidad

## Conexiones
- [[wiki/negocios/educacion-musical]] — negocio que lo usa
- [[wiki/canales/instagram-mercadoernesto]] — cuenta donde opera
- [[wiki/canales/meta-ads]] — pauta que genera los comentarios con la keyword
