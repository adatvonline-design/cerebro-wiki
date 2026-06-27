# Guía de Migración — Claude + Obsidian + GitHub

Paso a paso para reconstruir el sistema en cualquier computadora nueva.

---

## PARTE 1 — Instalar las herramientas base

### 1. Obsidian
- Descargar en: https://obsidian.md/download
- Instalar normalmente
- Al abrir: elegir "Open folder as vault" (NO crear vault nuevo)

### 2. Claude Code (CLI)
- Instalar Node.js primero si no lo tienes: https://nodejs.org
- En terminal/PowerShell:
  ```
  npm install -g @anthropic-ai/claude-code
  ```
- Iniciar sesión:
  ```
  claude
  ```
  Te pedirá autenticarte con tu cuenta de Anthropic

### 3. Git
- Descargar en: https://git-scm.com/download/win
- Instalar con opciones por defecto
- Verificar: `git --version` en terminal

---

## PARTE 2 — Restaurar el wiki desde GitHub

### 4. Clonar el repositorio de Cerebro
En la carpeta donde quieras tener Obsidian (ej. Documentos):
```
git clone https://github.com/adatvonline-design/cerebro-wiki.git
```
Esto descarga todo el wiki con historial completo.

### 5. Abrir en Obsidian
- Abrir Obsidian → "Open folder as vault"
- Seleccionar la carpeta `cerebro-wiki` recién clonada
- El wiki aparece completo con todas las páginas y conexiones

---

## PARTE 3 — Restaurar la memoria de Claude Code

### 6. Copiar la carpeta `.claude`
Desde tu computadora anterior (o respaldo):
```
C:\Users\TU_USUARIO\.claude\
```
Copiar esa carpeta completa al mismo path en la nueva máquina.

Si no tienes respaldo de `.claude`, Claude Code arranca sin memoria previa — el wiki en Obsidian conserva todo el conocimiento de negocio, así que la pérdida es mínima.

---

## PARTE 4 — Configurar Claude Code para usar el wiki

### 7. Iniciar Claude Code apuntando al directorio de trabajo
```
cd C:\Users\TU_USUARIO\Documentos\Claude
claude
```

### 8. Verificar que lee el CLAUDE.md
Claude Code carga automáticamente el `CLAUDE.md` de la carpeta de trabajo. Este archivo ya tiene la referencia al vault de Obsidian en `Cerebro/`.

### 9. Primera sesión — decirle a Claude que lea el wiki
Al inicio de cada sesión nueva, escribir:
```
Lee el wiki y dime el estado actual del negocio.
```
Claude leerá CLAUDE.md + index.md + log.md y reportará donde quedamos.

---

## PARTE 5 — Mantener el respaldo actualizado

### 10. Después de cada sesión de trabajo con el wiki
En terminal, desde la carpeta del wiki:
```
cd C:\Users\TU_USUARIO\Documentos\cerebro-wiki
git add .
git commit -m "Wiki update YYYY-MM-DD"
git push
```

O pedirle a Claude que lo haga: "Haz commit y push del wiki."

---

## Resumen de URLs y rutas importantes

| Qué | Dónde |
|---|---|
| Wiki local | `C:\Users\Dell\Documents\obsidian\Cerebro\` |
| Respaldo en GitHub | `https://github.com/adatvonline-design/cerebro-wiki` |
| Memoria de Claude | `C:\Users\Dell\.claude\` |
| Directorio de trabajo Claude | `C:\Users\Dell\Documents\Claude\` |
| Schema del wiki | `Cerebro\CLAUDE.md` |
| Índice del wiki | `Cerebro\index.md` |
| Log del wiki | `Cerebro\log.md` |

---

## Lo que se pierde y lo que NO se pierde en una migración

| | Se pierde | Se conserva |
|---|---|---|
| **Wiki completo** | — | ✓ Vía GitHub |
| **Historial de cambios** | — | ✓ Git history |
| **Memoria de Claude** | Si no respaldas `.claude\` | ✓ Si copias la carpeta |
| **Historial de conversaciones** | ✓ (no se respalda) | — |
| **Configuración de Obsidian** | Plugins/temas | ✓ El contenido |

> La única pérdida real son los historiales de conversación de Claude. El conocimiento ya está capturado en el wiki, así que el impacto es mínimo.

---

## Pendiente: subir el repo a GitHub

El repo local ya está creado en `Cerebro/.git`. Para activar el respaldo en la nube:

1. Ir a https://github.com/new
2. Nombre: `cerebro-wiki`
3. **Privado** ✓
4. NO inicializar con README
5. Click "Create repository"
6. En terminal:
   ```
   cd "C:\Users\Dell\Documents\obsidian\Cerebro"
   # Ya configurado — repo activo en:
   # https://github.com/adatvonline-design/cerebro-wiki
   ```
