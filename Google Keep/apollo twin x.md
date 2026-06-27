
1. El Hardware Necesario (Indispensable)
La Z590-A PRO requiere una tarjeta de expansión (AIC) para habilitar Thunderbolt.
Tarjeta Requerida: Necesitas la MSI Thunderbolt 4 PCIe Expansion Card.
Instalación: Debe ir en la ranura PCIe inferior que sea compatible y conectarse al encabezado JTPWR1 y JTBT1 de tu tarjeta madre usando los cables que vienen con la tarjeta de expansión.
Cable: Asegúrate de usar un cable Thunderbolt 3 o 4 certificado (no un cable USB-C de carga genérico, ya que no tienen el ancho de banda necesario).
2. Configuración en la BIOS
Una vez instalada la tarjeta física, debes "avisarle" a la PC que la use:
Reinicia y entra a la BIOS (tecla Supr o F2).
Ve a Settings > Advanced > Thunderbolt(TM) Configuration.
Cambia Discrete Thunderbolt(TM) Support a Enabled.
Asegúrate de que el Security Level esté en No Security (User Authorization a veces causa problemas de detección inicial con Universal Audio).
3. Instalación de Software en Windows
Windows no gestiona Thunderbolt de forma tan nativa como macOS, así que el orden importa:
Driver de Intel: Instala el Intel Thunderbolt Control Center desde la página de soporte de MSI o de Intel.
Software de UAD: Descarga e instala UAD Software v11 (o la versión más reciente) desde el sitio oficial de Universal Audio.
Firmware: Al conectar la Apollo por primera vez, es muy probable que te pida una actualización de firmware. No desconectes el cable durante este proceso.
4. Optimización para Audio (Evitar Clics y Pops)
Las PC con Windows suelen tener funciones de ahorro de energía que interrumpen el flujo de Thunderbolt:
Plan de Energía: Ve a Panel de Control > Opciones de Energía y selecciona Alto Rendimiento.
Administrador de Dispositivos: Busca los controladores Thunderbolt y en la pestaña de "Administración de energía", desmarca la opción "Permitir que el equipo apague este dispositivo para ahorrar energía".

Nota sobre adaptadores: Si tu Apollo es el modelo con conexión Thunderbolt 2 (mini DisplayPort), necesitarás adicionalmente el adaptador de Thunderbolt 3 a Thunderbolt 2 de Apple, que es el único que Universal Audio garantiza que funciona bidireccionalmente.
