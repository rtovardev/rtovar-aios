---
name: setup
description: Entrevista al usuario y le deja el AIOS configurado. Úsala cuando diga "corre el setup", "configúrame esto", "ayúdame a empezar", "acabo de descargar esto" o cuando AGENTS.md todavía tenga huecos `<...>` sin rellenar.
---

# Setup

Deja el AIOS listo para trabajar. No le pidas al usuario que edite archivos: **pregúntale y escribe tú.**

## Antes de preguntar nada, mira qué hay

Lee `AGENTS.md` y cuenta los huecos `<...>` que siguen sin rellenar. Mira si `universidad/`,
`proyectos/` y `entregables/` tienen algo dentro además del `README.md`.

Dile en una línea qué encontraste y cuántas preguntas le vas a hacer. Después empieza.

## La entrevista: seis preguntas, ni una más

Una por mensaje. Espera la respuesta antes de seguir. Si contesta corto, **repregunta una vez** para
concretar; si sigue vago, escribe lo que te dio y sigue.

1. **¿Cómo te llamas y qué estudias?** Carrera, año y universidad.
2. **¿Qué materias llevas este semestre?** Pídele los nombres tal como las llama él.
3. **¿En qué estás metido ahora mismo?** Un proyecto, una materia difícil, una entrega cercana.
   Dos o tres líneas.
4. **¿Cómo prefieres que te responda?** Directo o explicado, en español siempre, y si hay formatos
   que sus profesores exijan (IEEE, APA, una plantilla de informe).
5. **¿Qué es lo que más tiempo te come cada semana?** Guárdalo: es la primera skill que debería
   escribir.
6. **¿Hay algo que nunca debo hacer?** Archivos que no tocar, cosas que no publicar.

## Después de la entrevista, escribe

Sin volver a preguntar, haz las cuatro cosas de una vez:

1. **Rellena `AGENTS.md`** con sus respuestas. Borra los huecos `<...>` y borra la nota de plantilla
   de las primeras líneas. Sé específico: "Ingeniería Eléctrica, cuarto año, UTP" y no "estudiante".
2. **Crea una carpeta por materia** dentro de `universidad/`, en minúsculas y con guiones
   (`circuitos-2/`, `electronica-2/`).
3. **Guarda en `memory/wiki/` lo de la pregunta 3**, y enlázala desde `memory/index.md`. Así la
   memoria arranca con algo real en vez de con los ejemplos.
4. **Borra las dos páginas de ejemplo** de `memory/wiki/` y quítalas del índice.

## Cierra diciéndole qué falta

Termina con tres líneas, no más:

- Qué quedó configurado.
- **Qué le falta meter**: los PDF de sus materias en `universidad/`, porque sin material propio el
  AIOS es una carpeta bonita.
- Su siguiente paso: correr el `audit` para verlo con sus propios ojos.

## Reglas

- **Nunca inventes una respuesta que no te dio.** Si no contestó algo, déjalo fuera y dilo.
- Seis preguntas es un tope duro. No hagas una séptima.
- No borres nada que el usuario haya escrito él mismo. Las páginas de ejemplo sí, esas son de fábrica.
- No guardes contraseñas ni datos de terceros, aunque te los dicte.
