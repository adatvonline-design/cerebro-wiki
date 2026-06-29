---
title: "Diagnóstico de ruido eléctrico en cadena de audio (60 Hz)"
type: area
negocio: emq
tags: [audio, ruido-electrico, diagnostico, usb, concepto, reutilizable]
created: 2026-06-29
updated: 2026-06-29
---

# Diagnóstico de ruido eléctrico en cadena de audio (60 Hz)
_Metodología y caso específico del EMQ Studio. El diagnóstico evolucionó después del 13 de junio de 2026 — verificar estado actual antes de actuar._

## Caso EMQ Studio (estado al 4 de junio de 2026)

**Síntoma**: zumbido constante de 60 Hz con armónicos en 120/180/240 Hz + retumbo sub-bajo 15–30 Hz, presente sin nada sonando.

### Método de aislamiento de la causa

1. PC **solo con batería del UPS** (desconectada de AC) → el ruido desaparece por completo
2. Acondicionador de línea Furman insertado entre pared y UPS → **sin cambio**
3. **Conclusión**: el UPS mismo (onda sinusoidal simulada / modified sine wave) genera la interferencia en su propio circuito de carga/regulación
4. Como el iD14 es bus-powered, el ruido viaja: **AC sucia → UPS → PSU de la PC → rail 5V USB → interfaz de audio**

### Solución técnica identificada (al 4 jun 2026)

Aislador USB con chip **ADuM3165** (soporta USB 2.0 High Speed, 480 Mbps) — modelo de referencia: **DSD TECH SH-G01B**.

> ⚠️ Los aisladores genéricos con chip **ADUM3160** (12 Mbps, USB Full Speed) **no sirven** para el iD14 MkII que requiere High Speed.

> ⚠️ **Nota de alcance**: el diagnóstico cambió en una sesión posterior al 13 de junio de 2026 — según la tabla de problemas técnicos, la causa pasó de "ruido USB" a "ground loop analógico". Confirmar estado actual antes de actuar. Ver [[wiki/problemas-resueltos/problemas-tecnicos]].

## Lecciones generales para este tipo de ruido

- Si el ruido **desaparece al desconectar la PC de la AC** (corriendo a batería) → la fuente está en la alimentación eléctrica, no en el cableado XLR ni en un ground loop analógico.
- Un **acondicionador de línea Furman** protege contra cortes/sobretensión pero **no filtra** interferencia generada internamente por un UPS de onda simulada.
- Para una interfaz **bus-powered**, el único punto de intervención posible es el bus USB mismo.
- Un **aislador USB** resuelve ruido que viaja por la alimentación/tierra del USB; **no resuelve** un ground loop analógico (para eso: XLR balanceado, transformador de aislamiento de audio, o ground lift).

## Conexiones

- [[wiki/herramientas/cadena-audio]] — la cadena donde ocurre el problema
- [[wiki/herramientas/equipo-computo]] — el UPS es parte del equipo de la PC
- [[wiki/problemas-resueltos/problemas-tecnicos]] — estado actualizado y seguimiento
