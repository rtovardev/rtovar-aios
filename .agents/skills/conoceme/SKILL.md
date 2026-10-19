---
name: conoceme
description: Entrevista de bienvenida que deja el sistema configurado para el usuario. Úsala cuando diga "/conoceme", "conóceme", "entrevístame", "empecemos", "configúrame esto", "acabo de descargar esto", en la primera sesión, o cuando AGENTS.md todavía tenga huecos `<...>` sin rellenar.
---

# Conóceme

Es lo primero que hace alguien con su sistema nuevo. No le pidas que edite archivos: **pregúntale y escribe tú.**

## Antes de preguntar, mira qué hay

Lee `AGENTS.md` y cuenta los huecos `<...>`. Mira si `universidad/`, `proyectos/` y `memory/wiki/` tienen algo además de los archivos de ejemplo.

Abre con tres líneas, no más:

1. Qué es esto: «Este es tu sistema operativo de IA. Lo que me digas ahora queda escrito y lo voy a leer cada vez que trabajemos».
2. Qué encontraste (por ejemplo, «está recién estrenado» o «ya tiene tu nombre, faltan tus materias»).
3. Cuántas preguntas vas a hacer.

Si `AGENTS.md` ya no tiene huecos, pregunta solo lo que falte o esté desactualizado.

## La entrevista: ocho preguntas como máximo

Una por mensaje. Espera la respuesta. Si contesta muy corto, **repregunta una vez** para concretar; si sigue vago, anota lo que te dio y sigue.

1. **¿Cómo te llamas y qué estudias?** Carrera, año y universidad.
2. **¿Qué materias llevas este semestre?** Los nombres tal como las llama.
3. **¿En qué estás metido ahora?** Proyectos, entregas cercanas, una materia difícil. Dos o tres líneas.
4. **¿Qué quieres lograr este semestre?** Una o dos metas.
5. **¿Cómo prefieres que te responda?** Directo o explicado, y formatos que te exijan (APA, IEEE, una plantilla de informe).
6. **¿Qué tarea repites cada semana y te quita más tiempo?** Es la candidata a primera skill.
7. **¿Qué herramientas usas a diario?** Correo, calendario, GitHub, Notion, Drive… Sirve para `/conectar`.
8. **¿Hay algo que nunca deba hacer?** Archivos que no tocar, cosas que no publicar.

## Después de la entrevista, escribe

Sin volver a preguntar, haz todo de una vez:

1. **Rellena `AGENTS.md`**: borra los huecos `<...>` y la nota de plantilla del inicio. Sé específico: «Ingeniería de Sistemas, tercer año, UTP», no «estudiante».
2. **Crea una carpeta por materia** en `universidad/` (minúsculas y guiones: `bases-de-datos-2/`) y una por proyecto en `proyectos/` con su `NOTAS.md` de dos líneas.
3. **Crea `memory/wiki/perfil.md`** con metas, preferencias, la tarea que repite (pregunta 6) y sus herramientas (pregunta 7). Usa el formato de `memory/wiki/ejemplo.md`, con fechas de hoy.
4. **Enlázala desde `memory/index.md`** y, si ya existe una página real, borra `ejemplo.md` y su enlace.

## Cierra

Cuatro líneas:

- Qué quedó escrito y dónde.
- Qué le falta meter: material propio (PDF, apuntes) en `universidad/`.
- Su primera skill candidata, con la tarea de la pregunta 6: «cuando quieras, corre `/crear-skill`».
- El siguiente paso: `/audit` para ver cómo quedó.

## Reglas

- **Nunca inventes una respuesta que no te dio.** Si no contestó algo, déjalo fuera y dilo.
- Ocho preguntas es un tope duro.
- No borres nada que el usuario haya escrito. Las páginas de ejemplo sí: son de fábrica.
- No guardes contraseñas, números de documento, datos de salud ni datos de otras personas, aunque te los dicte. Si aparecen, dile que no los vas a guardar.
