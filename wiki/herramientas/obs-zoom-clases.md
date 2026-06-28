---
title: "OBS + Zoom para clases online"
type: herramienta
negocio: educacion
tags: [clases-online, obs, zoom, ableton, audio, streaming]
created: 2026-06-28
updated: 2026-06-28
---

# OBS + Zoom para clases online
_Setup técnico para impartir clases en línea con audio de calidad desde DAW o micrófono._

## Arquitectura general

```
Ableton / micrófono → OBS (con Virtual Camera) → Zoom
Audio routing: VoiceMeeter Banana → Cable Virtual A/B
```

## Configuración paso a paso

1. **OBS** actúa como fuente de video y audio con Virtual Camera activada
2. A cada entrada de audio en OBS se le agrega filtro **Monitor de Audio** → ruteado a *Cable A*
3. En Propiedades de Audio de OBS: *Audio escritorio* → *Cable B*
4. **Zoom**: entrada de audio = *Cable A* · salida = *Cable B*
5. Ableton/VoiceMeeter: usar ASIO virtual, con monitor en OBS ruteado a *Cable A*

## Ajustes de latencia

- Micrófono de cañón: agregar ~200 ms de latencia de sync en OBS
- Audio escritorio: agregar ~400–950 ms (verificar con metrónomo hablado)

## Calidad de video en Zoom

Para lograr 1080p en Zoom via OBS:
- Referencia: https://jkudo.medium.com/how-to-achieve-zoom-full-hd-1080p-1920-1080-delivery-with-obs

## Herramientas complementarias

- **Piano From Above**: https://piano-from-above.software.informer.com/ — visualización de piano en pantalla para clases
- **VoiceMeeter Banana**: routing de audio avanzado entre apps
- **LightHost** (efectos VST en VoiceMeeter): https://github.com/rolandoislas/LightHost/releases

## Limitaciones conocidas

- Al rutear audio de Ableton a Zoom mediante OBS, **desactivar salidas (B) de VoiceMeeter** para evitar feedback
- La configuración de OBS Virtual Camera debe activarse antes de abrir Zoom

## Pendientes

> ⚠️ Pendiente: Verificar setup con nueva configuración del estudio.

## Conexiones
- [[wiki/negocios/educacion-musical]] — clases en línea como modalidad activa
