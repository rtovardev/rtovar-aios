---
name: crear-skill
description: Convierte un workflow que el usuario repite en una skill nueva, desde identificar la tarea hasta probar que se activa sola. Úsala cuando diga "/crear-skill", "crea una skill", "quiero automatizar esto", "haz esto una skill", "siempre hago lo mismo", o cuando notes que repite la misma tarea por tercera vez.
---

# Crear una skill

Una skill es la instrucción de **cómo se hace bien una tarea que vale la pena repetir**. No es un programa: es texto que el agente sigue igual la décima vez que la primera.

## 1. Encuentra el workflow

Si el usuario ya trae la tarea, pasa al paso 2. Si no:

- Lee `memory/wiki/perfil.md` (la tarea que dijo repetir en `/conoceme`), `universidad/` y `proyectos/`.
- Propón dos o tres candidatas concretas, con por qué cada una.
- Si nada encaja, ofrece estas para adaptar: `resumir-clase`, `informe-laboratorio`, `plan-de-estudio`, `preparar-exposicion`, `revisar-codigo`.

Regla de las tres veces: lo que explicó dos veces va en `AGENTS.md`; lo que hizo tres veces es una skill.

## 2. Descompón el workflow

Hazle estas cuatro preguntas, una a la vez. Sin ellas la skill no está lista.

1. **¿Cuándo se usa?** Las palabras exactas con que la pediría. Es lo más importante: una skill que no se dispara no existe.
2. **¿Qué recibe y qué entrega?** De dónde salen los datos (qué carpeta, qué archivo) y cómo se ve el resultado.
3. **¿Qué distingue un buen resultado de uno mediocre?** El criterio que usaría él para revisarlo.
4. **¿Qué no debe hacer?** Qué no tocar, qué no publicar, qué no asumir.

## 3. Escríbela

Crea `.agents/skills/<nombre>/SKILL.md`. El nombre va en minúsculas con guiones y **debe ser igual** al `name` del frontmatter, o OpenCode no la carga.

```markdown
---
name: resumir-clase
description: Resume el PDF de una clase con ideas, fórmulas y lo que huele a examen. Úsala cuando el usuario diga "resume esta clase", "hazme un resumen del tema" o comparta un PDF de universidad/.
---

# Resumir una clase

## Cómo hacerlo
1. …

## Cómo saber que quedó bien
- …

## Qué no hacer
- …
```

Para la `description`:

- ❌ `description: Ayuda con resúmenes.` No dice cuándo; nunca se activa.
- ✅ `description: <qué hace>. Úsala cuando el usuario diga "<frase 1>", "<frase 2>" o <situación>.`

Para el cuerpo:

- Instrucciones, no explicaciones: «Verifica que cada resultado tenga unidades», no «es importante que tengan unidades».
- Pasos numerados y un criterio de calidad concreto.
- Corta: si pasa de una pantalla, probablemente son dos skills.

## 4. Pruébala

1. Muéstrale la skill completa.
2. Dile que **cierre y vuelva a abrir OpenCode** para que la cargue.
3. Que la pida **sin nombrarla**, con una de las frases de la descripción.
4. Si no se activó, agrega a la `description` las palabras exactas que usó y repite.

Una skill que nunca se ejecutó no está terminada. Cuando funcione, anótala en `memory/wiki/perfil.md` y agrégala a la tabla de `SKILLS.md` en la sección «Mis skills».

## Reglas

- No sobrescribas una skill existente sin preguntar.
- No copies en la skill datos sensibles del usuario: la skill puede terminar compartida.
