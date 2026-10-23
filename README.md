# rtovar-aios · tu sistema operativo de IA

Una carpeta donde tu agente de IA sabe quién eres, recuerda lo que importa y sabe hacer lo que le enseñes. Funciona con [OpenCode](https://opencode.ai) (gratis, de código abierto), Codex y Claude Code.

## Qué es un sistema operativo de IA

Un chat empieza de cero cada vez. Este sistema acumula, en tres capas de texto plano:

| Capa | Dónde vive | Qué hace |
|---|---|---|
| Contexto | `AGENTS.md` | Quién eres, qué estudias y cómo quieres que trabaje. El agente lo lee siempre. |
| Memoria | `memory/` | Lo que sobrevive al cerrar la ventana: una wiki con un índice. |
| Capacidades | `.agents/skills/` | Tareas que le enseñaste una vez y repite igual. Ver [SKILLS.md](SKILLS.md). |

Y se conecta a tus apps (calendario, correo, GitHub) a través de un gateway de herramientas, [Composio](https://composio.dev).

Todo es texto: lo lees, lo editas y te lo llevas. Ninguna herramienta es dueña de tu sistema.

## Empezar en 10 minutos

### 1. Instala OpenCode

Usa la versión 1 (1.19.3). La versión 2 cambió la configuración y todavía no se instala con gestores de paquetes en Windows.

```bash
# macOS o Linux
curl -fsSL https://opencode.ai/install | bash

# Windows (PowerShell, con Node.js instalado)
npm i -g opencode-ai@1.19.3
```

Comprueba con `opencode --version`. OpenCode trae modelos gratuitos que no piden cuenta ni tarjeta; la plantilla ya elige uno en `opencode.json`.

### 2. Clona la plantilla

```bash
git clone https://github.com/rtovardev/rtovar-aios.git mi-sistema
cd mi-sistema
opencode
```

Sin git: botón verde **Code → Download ZIP**, descomprime y abre OpenCode dentro de la carpeta. Lo importante es abrir el agente **dentro** de la carpeta: ahí ve todo.

### 3. Deja que te entreviste

```
/conoceme
```

Una pregunta a la vez. Al terminar, `AGENTS.md` tiene tus datos, hay una carpeta por materia y tu memoria tiene su primera página.

### 4. Pídele que se audite

```
/audit
```

Te da un puntaje sobre 100 y tres mejoras. Aplica una (el audit puede hacerlo por ti, siempre con tu permiso) y vuelve a correrlo.

## Después

| Cuando quieras… | Corre |
|---|---|
| Conectar tu calendario, correo o GitHub | `/conectar` |
| Saber qué tienes hoy | `/brief` |
| Convertir algo que repites en una skill | `/crear-skill` |
| Aprender un tema en varias sesiones | `/teach` |
| Que te interrogue un plan | `/grill-me` |
| Guardar lo de hoy antes de cerrar | `/cerrar-sesion` |

No hace falta escribir el comando: pide lo que quieres en español («qué tengo hoy», «resume esta clase») y el agente elige la skill por su descripción.

### Para que crezca contigo

- **Hoy:** mete material tuyo (los PDF de una materia en `universidad/`). Un sistema vacío es una carpeta bonita.
- **Esta semana:** úsalo para una entrega real.
- **Cada dos semanas:** `/audit` y aplica una mejora.
- **La tercera vez que hagas algo:** `/crear-skill`.

## Seguridad

- Los permisos de `opencode.json` piden tu aprobación antes de editar archivos, correr comandos o usar herramientas externas. No abras OpenCode con `--yolo`.
- Antes de aprobar una acción externa, lee su nombre. Si dice SEND, CREATE, UPDATE o DELETE, piénsalo dos veces.
- Tu clave de Composio va en una variable de entorno (`COMPOSIO_CONSUMER_KEY`), nunca en un archivo del repo. `/audit` revisa que no haya claves sueltas.
- Si vas a subir tu sistema a GitHub, hazlo en un repo **privado**: tu memoria es tuya.

## Otros harnesses

| Harness | Contexto | Skills | Comandos |
|---|---|---|---|
| OpenCode 1 | `AGENTS.md` + `memory/index.md` (por `opencode.json`) | `.agents/skills/` | `.opencode/commands/` (`/conoceme`, `/audit`…) |
| Codex | `AGENTS.md` | `.agents/skills/` | `$conoceme` o `/skills` |
| Claude Code | `CLAUDE.md` → `@AGENTS.md` | `.claude/skills/` (enlace a `.agents/skills/`) | `/conoceme` |

En Windows, git puede clonar el enlace `.claude/skills` como un archivo de texto. Solo afecta a Claude Code: copia la carpeta `.agents/skills` a `.claude/skills`.

## Estructura

```
mi-sistema/
├── AGENTS.md            contexto que el agente lee siempre
├── CLAUDE.md            puente para Claude Code
├── opencode.json        modelo, permisos y Composio
├── SKILLS.md            catálogo de skills
├── memory/              index.md + wiki/
├── universidad/         una carpeta por materia
├── proyectos/           uno por carpeta, con NOTAS.md
├── entregables/         lo terminado
├── .agents/skills/      las skills
└── .opencode/commands/  los /comandos de OpenCode
```

## Licencia

MIT. Las skills `teach`, `grilling`, `grill-me` y `research` son de sus autores, también con licencia MIT: ver [THIRD_PARTY.md](THIRD_PARTY.md).
