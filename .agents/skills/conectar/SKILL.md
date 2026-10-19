---
name: conectar
description: Guía paso a paso para conectar el sistema a apps externas (Google Calendar, Gmail, GitHub, Notion, Drive…) a través de Composio. Úsala cuando el usuario diga "/conectar", "conecta mi calendario", "conecta mi correo", "quiero conectar mis apps", "configura Composio" o pregunte cómo darle acceso al agente a una herramienta.
---

# Conectar

Conecta el sistema a las apps del usuario por un **gateway de herramientas**: un solo servidor MCP (Composio) desde el que se autoriza cada app. Avanza un paso a la vez y espera a que el usuario confirme antes del siguiente.

## Antes de empezar

- Lee `opencode.json` y `memory/wiki/conexiones.md` (si existe). Si Composio ya está habilitado, salta al paso 4.
- Dile en una línea qué vas a hacer y que la meta mínima es **una app conectada**.

## Paso 1 · Cuenta y clave

Pídele que haga esto él, en el navegador:

1. Entrar a https://composio.dev y crear una cuenta con su **Gmail personal** (el correo de la universidad puede bloquear la autorización). El plan gratuito no pide tarjeta.
2. En el dashboard, abrir **AI Clients** y copiar su **consumer API key**.

**No le pidas que pegue la clave en el chat.** Lo que se escribe aquí puede quedar en el historial.

## Paso 2 · Guardar la clave en su computadora

La clave va en una variable de entorno, fuera del repositorio. Dale el comando según su sistema y que lo corra él en otra terminal:

```bash
# macOS / Linux (zsh); en bash usa ~/.bashrc
echo 'export COMPOSIO_CONSUMER_KEY="pega-aqui-tu-clave"' >> ~/.zshrc && source ~/.zshrc
```

```powershell
# Windows (PowerShell)
setx COMPOSIO_CONSUMER_KEY "pega-aqui-tu-clave"
```

En Windows, `setx` solo aplica a terminales nuevas: hay que cerrar y abrir la terminal.

## Paso 3 · Habilitar Composio

Pide permiso y cambia en `opencode.json` el bloque `mcp.composio` a `"enabled": true`. No cambies nada más.

Luego pídele que cierre OpenCode y lo vuelva a abrir **en esta carpeta, desde una terminal nueva**, y que corra:

```bash
opencode mcp list
```

Composio debe aparecer conectado. Si no:
- `opencode mcp debug composio` muestra el error.
- Si dice que falta la clave, la variable no llegó a esta terminal: repetir el paso 2 y abrir una terminal nueva.

## Paso 4 · Conectar la primera app

Cuando vuelva, pregúntale cuál conectar primero (sugiere Google Calendar). Usa la herramienta de Composio que gestiona conexiones para generar el enlace de autorización, dáselo, y espera a que autorice en el navegador y vuelva al chat.

Comprueba con **una lectura simple**: los eventos de hoy, o los tres últimos asuntos del correo. Muéstrale el resultado.

Si sobra tiempo, repite con una segunda app.

## Paso 5 · Registrar

Crea o actualiza `memory/wiki/conexiones.md` con: qué apps están conectadas, la fecha y para qué las usa. **Sin claves ni correos.** Enlázala desde `memory/index.md`.

Cierra con: «Prueba `/brief` para ver tu día».

## Plan B · sin MCP

Si el MCP no conecta, la CLI de Composio sirve igual:

```bash
curl -fsSL https://composio.dev/install | sh   # luego abrir una terminal nueva
composio login              # si no hace nada: composio logout y luego composio login --no-wait
composio link googlecalendar
composio search "list today's calendar events"
composio execute <SLUG> --dry-run -d '{...}'
```

## Reglas

- **Leer antes que escribir.** Para comprobar una conexión, solo lecturas.
- Nunca ejecutes una acción que mande, cree, actualice o borre algo sin que el usuario la apruebe explícitamente, aunque OpenCode ya te esté pidiendo permiso.
- Nunca escribas claves en archivos del repositorio. Si el usuario pega una en el chat, dile que la regenere en el dashboard.
- Si algo falla dos veces, para, dile qué falló y ofrece el plan B. No improvises cambios en la configuración.
