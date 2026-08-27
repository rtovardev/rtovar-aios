# Contexto de mi AIOS

> Este archivo se lee **siempre**, en cada conversación. Es lo que separa un chat de un sistema.
> Rellena los huecos `<...>` y borra los ejemplos. Sé específico: lo vago no ayuda al agente.

## Quién soy

- **Nombre:** `<tu nombre>`
- **Estudio:** `<carrera>`, `<año>`, `<universidad>`
- **Materias de este semestre:** `<lista corta>`
- **Idioma de trabajo:** español. Los nombres de archivos y el código van en inglés.

## En qué estoy trabajando

`<Dos o tres líneas sobre lo que tienes entre manos ahora mismo: un proyecto, una materia difícil,
una tesis, un trabajo. Actualiza esto cuando cambie — es lo que más rápido queda desactualizado.>`

## Cómo está organizado esto

Este directorio es mi espacio de trabajo completo. Todo lo mío vive aquí dentro:

- `universidad/` — una carpeta por materia: apuntes, guías, PDF del profesor, laboratorios.
- `proyectos/` — lo que estoy construyendo.
- `entregables/` — lo que ya está terminado y listo para entregar.
- `memory/` — lo que debes recordar entre conversaciones.
- `skills/` — lo que sabes hacer.

Cuando te pida algo, **primero mira si el material ya está aquí adentro** antes de pedírmelo o de
asumirlo. Si no encuentras algo que debería existir, dímelo.

## Cómo quiero que trabajes

- Responde directo. Sin introducciones ni resúmenes de lo que te pedí.
- Si algo es ambiguo, pregunta antes de asumir.
- Antes de una respuesta larga, dime en una línea qué vas a hacer.
- Cuando uses una fuente, cítala. **Si algo no está en las fuentes que te di, dilo en lugar de
  completarlo.**
- No inventes datos, fechas ni referencias bibliográficas. Nunca.

## Qué NO debes hacer

- No borres ni sobrescribas archivos sin preguntarme primero.
- No publiques nada en internet a mi nombre sin que yo lo apruebe.
- No guardes contraseñas, tokens ni datos personales de otras personas dentro de este directorio.

## Memoria

Lo que deba recordarse entre conversaciones vive en `memory/`. Antes de una tarea que dependa de
contexto previo, lee `memory/index.md` y abre las páginas que hagan falta.

Cuando aprendamos algo que valga la pena conservar —una decisión, un dato estable, cómo funciona
algo— escríbelo en `memory/wiki/` y enlázalo desde el índice.

## Skills

Las capacidades reutilizables viven en `skills/`. Cada una es una carpeta con un `SKILL.md`, y
arriba de ese archivo hay una `description` que dice **cuándo** usarla.

**Antes de responderme a cualquier cosa que no sea una pregunta trivial, mira qué hay en `skills/`
y lee la `description` de cada una.** Si alguna aplica a lo que te acabo de pedir, ábrela y sigue
sus instrucciones al pie de la letra, aunque yo no la haya nombrado. Dime cuál estás usando.

Yo casi nunca voy a escribir el nombre de una skill. Voy a pedirte lo que quiero en español y tú
tienes que reconocerlo.

Si me ves haciendo la misma tarea por tercera vez, dímelo y propón convertirla en una skill.
