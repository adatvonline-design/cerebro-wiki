---
title: "Compatibilidad Thunderbolt — MSI Z590-A PRO"
type: area
negocio: emq
tags: [thunderbolt, msi, hardware, audio, concepto, reutilizable]
created: 2026-06-29
updated: 2026-06-29
---

# Compatibilidad Thunderbolt — MSI Z590-A PRO
_Rutas para agregar Thunderbolt a la placa madre del EMQ Studio y poder usar el Apollo Twin X._

## El problema

La **MSI Z590-A PRO** no tiene Thunderbolt nativo — su puerto USB-C es solo USB 3.2. Tiene un header interno **JTBT1 de 16 pines** con **pinout propietario de MSI**, lo que descarta tarjetas de otras marcas (ASUS ThunderboltEX, Gigabyte GC-Titan Ridge en uso normal con header).

## Las dos rutas que funcionan

| Opción | Tipo | Detalle | Precio aprox. |
|---|---|---|---|
| **MSI ThunderboltM4 8K** | Oficial | Thunderbolt 4, conector de 16 pines compatible directo con JTBT1, chipset Intel JHL8540, PCIe 3.0 x4, hasta 40 Gbps. Z590-A PRO listada explícitamente como compatible. **Descontinuada** — buscar en eBay, MercadoLibre, sparepartworld.com | $50–80 USD |
| **Gigabyte GC-Titan Ridge 2.0** | No oficial (hack) | Thunderbolt 3 (suficiente para Apollo Twin X). Se instala en PCIe x4 **sin conectar el header**. Se puentea manualmente el pin TBT_Force_PWR en el conector del header de la tarjeta para mantenerla encendida sin señal del motherboard. Interfaz debe conectarse **antes de encender el PC** (cold-plug, sin hotplug) | $50–70 USD |

## Trade-offs del hack (Gigabyte GC-Titan Ridge)

- Funciona bien para uso fijo de estudio (se enciende con la interfaz ya conectada)
- **Sin hotplug**: no se puede conectar/desconectar con el PC encendido
- No soportado oficialmente — sin garantía si algo falla (riesgo de daño al hardware real: bajo)
- Documentado por otros usuarios para interfaces de audio Thunderbolt

## Alternativa que evita el problema por completo

Cambiar a la versión **USB del Apollo Twin X** — conecta directo a los puertos USB 3.2 existentes sin hardware adicional.

> ⚠️ Pendiente: Decidir entre Apollo Twin X Thunderbolt (requiere tarjeta add-on) vs. Apollo Twin X USB (sin hardware adicional).

## Conexiones

- [[wiki/herramientas/cadena-audio]] — el Apollo Twin X es la interfaz en evaluación
- [[wiki/herramientas/equipo-computo]] — la placa madre afectada
