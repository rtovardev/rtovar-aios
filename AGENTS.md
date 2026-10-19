# Contexto de mi sistema

> Plantilla: este archivo se lee **siempre**, en cada conversación. Es lo que separa un chat de un sistema.
> No lo llenes a mano: corre `/conoceme` y el agente te entrevista y lo escribe por ti. Esta nota se borra sola.

## Quién soy

- **Nombre:** `<tu nombre>`
- **Estudio:** `<carrera>`, `<año>`, `<universidad>`
- **Materias de este semestre:** `<lista corta>`
- **Idioma de trabajo:** español neutro, tuteando. Los nombres de archivos y el código van en inglés.

## En qué estoy trabajando

`<Dos o tres líneas sobre lo que tienes entre manos ahora: un proyecto, una materia difícil, una entrega.
Es lo que más rápido se desactualiza: cámbialo cuando cambie.>`

## Cómo está organizado esto

Este directorio es mi espacio de trabajo. Todo lo mío vive aquí dentro:

- `universidad/`: una carpeta por materia, con apuntes, guías, PDF y laboratorios.
- `proyectos/`: lo que estoy construyendo, cada uno con su `NOTAS.md`.
- `entregables/`: lo terminado y listo para entregar.
- `memory/`: lo que debes recordar entre conversaciones. Empieza por `memory/index.md`.
- `.agents/skills/`: lo que sabes hacer. El catálogo está en `SKILLS.md`.

Cuando te pida algo, **primero mira si el material ya está aquí** antes de pedírmelo o asumirlo. Si no encuentras algo que debería existir, dímelo.

## Cómo quiero que trabajes

- Responde directo, sin introducciones ni resúmenes de lo que te pedí.
- Si algo es ambiguo, pregunta antes de asumir.
- Antes de una tarea larga, dime en una línea qué vas a hacer.
- Cuando uses una fuente, cítala. **Si algo no está en mis fuentes, dilo en lugar de completarlo.**
- No inventes datos, fechas ni referencias. Nunca.

## Herramientas externas

- **Leer antes que escribir.** Con mis apps conectadas (correo, calendario, GitHub…), consulta libremente, pero no mandes, crees, cambies ni borres nada sin que yo lo apruebe en ese momento.
- Antes de pedirme aprobación, dime qué acción vas a correr y sobre qué.

## Qué NO debes hacer

- No borres ni sobrescribas archivos sin preguntarme.
- No publiques nada a mi nombre sin que lo apruebe.
- No guardes contraseñas, claves de API ni datos personales de otras personas en este directorio.

## Memoria

Lo que deba recordarse vive en `memory/`. Antes de una tarea que dependa de contexto previo, lee `memory/index.md` y abre las páginas que hagan falta.

Cuando aprendamos algo que valga la pena conservar (una decisión, un dato estable, cómo funciona algo), escríbelo en `memory/wiki/` y enlázalo desde el índice. Al terminar una sesión larga, ofrece `/cerrar-sesion`.

## Skills

Las capacidades viven en `.agents/skills/`, una carpeta por skill con su `SKILL.md`. Arriba de cada una hay una `description` que dice **cuándo** usarla.

**Antes de responder cualquier cosa que no sea trivial, revisa las skills disponibles y lee sus descripciones.** Si alguna aplica a lo que te pedí, cárgala y sigue sus instrucciones aunque yo no la haya nombrado. Dime cuál estás usando.

Casi nunca voy a escribir el nombre de una skill: te voy a pedir lo que quiero en español y tú tienes que reconocerlo.

Si me ves haciendo la misma tarea por tercera vez, dímelo y propón `/crear-skill`.
