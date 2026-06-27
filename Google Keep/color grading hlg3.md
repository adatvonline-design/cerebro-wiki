
Configuración del proyecto: En la configuración del proyecto (Project Settings), ve a "Color Management".
Timeline Color Space: Configúralo a "Rec.709 Gamma 2.4" (o sRGB si es para web/computadoras).
Output Color Space: También a "Rec.709 Gamma 2.4".
Nodo de Transformación de Espacio de Color (Color Space Transform - CST): Este es el paso clave.
En tu primera o segunda nodo en la página de Color, aplica el efecto "Color Space Transform".
Input Color Space: BT.2020 (o Rec.2020)
Input Gamma: Rec.2100 HLG (o HLG ARIB STD-B76, si esa es la opción específica de tu cámara).
Output Color Space: Rec.709
Output Gamma: Rec.709 Gamma 2.4 (o sRGB si es para web).
Importante: Algunos recomiendan activar la opción para "compress saturation" o "tone mapping" si estás trabajando con HLG de 8 bits para evitar la saturación excesiva o "clipping" de color.
Adobe Premiere Pro:
