# Skills

Cada skill es una carpeta en `.agents/skills/` con un `SKILL.md`. El agente lee la `description` de cada una y decide cuál usar; no hace falta nombrarlas. Las que tienen comando también se pueden llamar con `/nombre`.

## Mantener el sistema

| Skill | Para qué | Pídela con |
|---|---|---|
| `conoceme` | Te entrevista y deja `AGENTS.md`, carpetas y memoria configurados. | `/conoceme`, «empecemos», «entrevístame» |
| `audit` | Escanea el sistema, da un puntaje sobre 100, propone tres mejoras y, si aceptas, las aplica. | `/audit`, «¿qué me falta?», «cómo mejoro esto» |
| `conectar` | Conecta tus apps (Calendar, Gmail, GitHub…) por Composio, paso a paso. | `/conectar`, «conecta mi calendario» |
| `crear-skill` | Convierte un workflow que repites en una skill nueva y la prueba. | `/crear-skill`, «siempre hago lo mismo» |
| `guardar-en-memoria` | Escribe una página de memoria y la enlaza en el índice. | «guarda esto en memoria», «acuérdate de esto» |
| `cerrar-sesion` | Guarda lo aprendido, lo decidido y lo pendiente antes de cerrar. | `/cerrar-sesion`, «terminé por hoy» |

## Aprender

| Skill | Para qué | Pídela con |
|---|---|---|
| `teach` | Te enseña un tema a lo largo de varias sesiones, con misión, recursos y registro de lo aprendido. De Matt Pocock. | `/teach` |
| `estudiar` | Quiz y explicaciones con el material de tus materias. | «tómame un quiz», «tengo examen de» |
| `grill-me` / `grilling` | Te interroga un plan o una idea hasta encontrar los huecos. De Matt Pocock. | `/grill-me`, «cuestiona mi plan» |

## Trabajar

| Skill | Para qué | Pídela con |
|---|---|---|
| `brief` | Tu día: pendientes del sistema y, si están conectados, calendario, correo y GitHub. Solo lee. | `/brief`, «qué tengo hoy» |
| `research` | Investiga una pregunta en fuentes primarias y guarda lo encontrado en un Markdown. De Matt Pocock. | «investiga…», «busca en la documentación» |
| `pagina-web` | Tu portafolio en HTML plano, publicable gratis. | «hazme una página», «quiero un portafolio» |

`teach`, `grill-me` y `research` están en inglés, tal como las publicaron sus autores. El agente te responde en español igual.

## Mis skills

Las que escribas con `/crear-skill` van aquí.

| Skill | Para qué | Pídela con |
|---|---|---|

## Para instalar después

Cuando la plantilla se te quede corta. **Antes de instalar una skill ajena, léela: es texto que tu agente va a obedecer.**

| Skill | Para qué | Dónde |
|---|---|---|
| `find-skills` | Busca skills publicadas para lo que necesitas. | [vercel-labs/skills](https://github.com/vercel-labs/skills) |
| `skill-creator` | Crea y mide skills más elaboradas, con pruebas. | [anthropics/skills](https://github.com/anthropics/skills) |
| `wayfinder` | Planea un proyecto grande como un mapa de decisiones. | [mattpocock/skills](https://github.com/mattpocock/skills) |
| `domain-modeling` | Ordena el vocabulario de un proyecto en un glosario. | [mattpocock/skills](https://github.com/mattpocock/skills) |

```bash
npx skills@latest add mattpocock/skills --skill wayfinder
```
