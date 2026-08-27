# Tu AIOS

Un **AIOS** es un sistema operativo de inteligencia artificial: un solo directorio desde el que
trabajas, donde vive tu contexto, tu memoria y tus capacidades, y desde el que un agente puede
actuar sobre todo lo que tienes dentro.

No es una carpeta de archivos. Es un espacio donde el agente **sabe quién eres**, **recuerda** lo
que importa y **sabe hacer** las tareas que tú le enseñaste.

## Por qué esto cambia las cosas

Un chat empieza de cero cada vez. Le explicas quién eres, qué estudias, qué necesitas — y mañana
otra vez. Un AIOS invierte eso: escribes el contexto una sola vez y todo lo demás se apoya en él.

| Sin AIOS | Con AIOS |
|---|---|
| Explicas tu contexto en cada conversación | Está escrito una vez, se lee siempre |
| Lo aprendido se pierde al cerrar el chat | Vive en `memory/` |
| Repites la misma tarea desde cero | Es una skill que se ejecuta igual cada vez |
| Copias y pegas entre el chat y tus archivos | El agente trabaja directo sobre tus carpetas |

## Estructura

```
.
├── AGENTS.md               ← quién eres y cómo quieres trabajar. Se lee siempre
├── universidad/            ← una carpeta por materia
├── proyectos/              ← lo que estás construyendo
├── entregables/            ← lo que sale terminado
├── memory/                 ← lo que el sistema recuerda entre conversaciones
│   ├── index.md
│   └── wiki/
└── skills/                 ← lo que el sistema sabe hacer
    ├── audit/              ← revisa tu sistema y te dice qué falta
    ├── brief/              ← qué tienes por delante
    ├── crear-skill/        ← te enseña a escribir las tuyas
    ├── estudiar/           ← te toma quiz sobre el material de tus materias
    ├── guardar-en-memoria/ ← escribe una página nueva y la enlaza en el índice
    └── pagina-web/         ← tu portafolio en HTML plano, publicable gratis
```

Las tres capas que lo sostienen son siempre las mismas: **contexto** (`AGENTS.md`), **memoria**
(`memory/`) y **capacidades** (`skills/`). El resto son tus carpetas de trabajo, y crecen contigo.

## Empezar en 5 minutos

1. Descarga esta carpeta y ponle tu nombre. Vivirá contigo un buen tiempo.
2. Abre `AGENTS.md` y rellena los huecos `<...>`. Sé concreto: *"Ingeniería Eléctrica, cuarto año,
   UTP"* sirve mucho más que *"soy estudiante"*.
3. Abre tu agente **dentro** de la carpeta — esto es lo importante, ahí es donde ve todo:
   ```bash
   cd mi-aios
   codex          # o: claude
   ```
4. Pídele que se revise a sí mismo:
   ```
   Corre el audit
   ```

Si el audit corre y te dice qué te falta, tu AIOS está vivo.

## Cómo crece

Mete tus cosas adentro. Los PDF de una materia en `universidad/`, el proyecto de laboratorio en
`proyectos/`. A partir de ahí el agente puede leerlos, relacionarlos y trabajar con ellos — porque
todo está en el mismo sitio y él ya sabe quién eres.

Tres reglas que hacen que esto funcione a largo plazo:

1. **Si te descubres explicando lo mismo dos veces, va en `AGENTS.md`.**
2. **Si vale la pena repetir la tarea, es una skill.** Escríbela la tercera vez que la hagas.
3. **Si no está en las fuentes, el agente debe decirlo.** Nunca dejes que rellene huecos por ti.

## Compatibilidad

`AGENTS.md` y el formato `SKILL.md` son estándares abiertos. Tu contexto, tu memoria y tus skills
se leen igual en Codex CLI, Claude Code, OpenClaw y Cursor. Si mañana cambias de herramienta, tu
AIOS se va contigo.

Un detalle real, probado: en **Codex** las skills se activan solas con solo pedir lo que quieres
("tengo examen, hazme preguntas"). En **Claude Code** a veces hay que nombrarlas ("usa la skill
estudiar"), porque busca las suyas en otra carpeta. Mismo archivo, mismo resultado, un pelo más de
fricción.

Eso es justamente el punto: las herramientas caducan, tu sistema no.

---

Creado para el taller **Los fundamentos de la IA que no caducan**, InnovaTech — Congreso IEEE
Estudiantil Panamá, agosto 2026. Ricardo Tovar · [github.com/rtovardev](https://github.com/rtovardev)
