---
title: "Problemas técnicos — diagnóstico y resolución"
type: area
negocio: todos
tags: [problemas-resueltos, diagnostico, hardware, software]
created: 2026-06-29
updated: 2026-06-29
---

# Problemas técnicos — diagnóstico y resolución
_Tabla de seguimiento de problemas técnicos identificados, diagnosticados y resueltos (o pendientes). Estado al 13 de junio de 2026 — algunos evolucionaron después._

> **Nota de alcance**: al menos el zumbido eléctrico (primera fila) cambió de diagnóstico en una sesión posterior al 13 jun 2026 — de "ruido USB" a "ground loop analógico". Verificar estado actual antes de actuar sobre esa entrada.

| Problema | Diagnóstico | Solución / camino | Estado |
|---|---|---|---|
| Zumbido eléctrico 60 Hz (armónicos 120/180/240 Hz) al grabar con Audient iD14 | **Dos fuentes simultáneas**: (1) rail USB 5V sucio del UPS → iD14 bus-powered; (2) ground loop analógico en la cadena XLR/línea. El hub USB redujo el ruido pero no lo eliminó — confirma la segunda fuente. Ver [[wiki/conceptos/diagnostico-ruido-electrico]] | Hub USB instalado (resuelve componente USB parcialmente). Componente analógica sin resolver: aislar desconectando XLR uno a uno; solución probable: transformador de aislamiento de audio o ground lift | ⚠️ Parcialmente resuelto — componente analógica pendiente |
| Trackball Kensington Expert Mouse se congela | Dos instancias del dispositivo en Windows; scripts apuntaban a la instancia "fantasma" inactiva | Script que ubica dinámicamente la instancia activa y corre `pnputil /restart-device` (no `Disable-PnpDevice`, falla con HRESULT 0x80041001 en HID en Win11) | ✅ Resuelto — script final guardado en el Desktop |
| Dos HDD con sectores defectuosos (WDC WD20EARX y ST2000LM007) | SMART con sectores pendientes/reasignados/irrecuperables | Respaldo de ≈700 GB vía Robocopy antes de retirar los discos | ✅ Resuelto (datos respaldados) |
| RAM corriendo a 2400 MHz en vez de 3000 MHz | XMP desactivado en BIOS | Activar XMP Profile 1 | ✅ Resuelto — quedó en DDR4-2933 |
| CPU con spikes térmicos hasta 93°C | Límites de potencia en "unlimited" (4096W) | PL1 125W / PL2 180W / Current Limit 140A en BIOS | ✅ Resuelto |
| Ruido mecánico en el cooler Scythe Fuma 2 | Desgaste de balero (ajuste de curva de ventiladores no eliminó el ruido) | Lubricar con aceite 3 en 1, o reemplazar por Arctic P12 PWM / Noctua NF-F12 PWM | ⚠️ Diagnóstico confirmado; reemplazo sin confirmar |
| Apollo Twin X (Thunderbolt) incompatible con la placa madre | Z590-A PRO no tiene Thunderbolt nativo; header JTBT1 propietario MSI | Tarjeta MSI ThunderboltM4 8K (oficial) o Gigabyte GC-Titan Ridge 2.0 (hack). Ver [[wiki/conceptos/compatibilidad-thunderbolt]] | ⚠️ Sin compra confirmada |
| Batería del Dell Latitude 5420 degradada a 52% | 33,075 mWh de 63,000 mWh de diseño | Limitar carga a 80% con Dell Power Manager; pasta térmica; reemplazo eventual | ⚠️ Recomendado, sin confirmar ejecución |
| Krita no detecta presión del lápiz Huion | Sin diagnosticar — pendiente conocer modelo exacto de Huion y SO | Pendiente de información | ❌ Sin resolver |
| WhatsApp mostraba el nombre como "Anastancio Pintor" en el Pixel 5 Pro | Probable desincronización de Contactos de Google entre dispositivos | Revisar/borrar contacto en Google Contacts, forzar sincronización, limpiar caché de WhatsApp | ⚠️ Sin confirmar resolución |
| Soundrop no mostraba el perfil correcto de "Nuages" al subir un cover | Al menos 5 artistas distintos llamados "Nuages" en streaming | Migrar a DistroKid (licenciamiento de covers + herramienta "Fixer"). Ver [[wiki/negocios/nuages]] | ⚠️ Recomendación entregada, sin confirmar migración |

## Conexiones

- [[wiki/herramientas/equipo-computo]] — hardware donde ocurren la mayoría de estos problemas
- [[wiki/herramientas/cadena-audio]] — cadena de audio afectada por el ruido eléctrico
- [[wiki/conceptos/diagnostico-ruido-electrico]] — análisis detallado del zumbido
- [[wiki/conceptos/compatibilidad-thunderbolt]] — análisis detallado del Apollo Twin X
- [[wiki/negocios/nuages]] — problema de distribución musical
