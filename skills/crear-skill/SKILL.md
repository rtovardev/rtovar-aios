---
name: crear-skill
description: Guía al usuario para escribir una skill nueva. Úsala cuando pida "crea una skill", "quiero automatizar esto", "haz esto una skill" o cuando detectes que repite una misma tarea por tercera vez.
---

# Crear una skill

Una skill es la documentación de **cómo se hace bien una tarea que vale la pena repetir**. No es un
programa: es una instrucción escrita para que el agente la siga igual de bien la décima vez que la
primera.

## Antes de escribirla, pregunta

No empieces a escribir sin estas cuatro respuestas. Si el usuario no las tiene claras, la skill no
está lista para existir todavía.

1. **¿Cuándo se usa?** Las palabras exactas con las que el usuario la pediría. Esto es lo más
   importante: una skill que no se dispara es una skill que no existe.
2. **¿Qué recibe y qué entrega?** De dónde salen los datos y cómo debe verse el resultado.
3. **¿Qué distingue un buen resultado de uno mediocre?** Aquí está el valor real de la skill.
   Cualquiera describe la tarea; el criterio de calidad es lo que se olvida.
4. **¿Qué NO debe hacer?** Los límites: qué no tocar, qué no publicar, qué no asumir.

## Estructura

Crea la carpeta `skills/<nombre-en-minusculas-con-guiones>/SKILL.md`:

```markdown
---
name: nombre-de-la-skill
description: Qué hace. Úsala cuando <disparadores concretos>.
---

# Título

Una frase sobre qué resuelve.

## Cuándo usarla
## Cómo ejecutarla
## Cómo verificar el resultado
## Reglas y límites
```

## Cómo escribir la descripción

Es el único campo que el agente lee para decidir si activarla. Debe contener **qué hace** y
**cuándo usarla**, con las palabras reales del usuario.

- ❌ `description: Ayuda con informes de laboratorio.`
  No dice cuándo. Nunca se va a activar.
- ✅ `description: Redacta y revisa informes de laboratorio siguiendo el formato de la facultad.
  Úsala cuando el usuario diga "informe de lab", "reporte de laboratorio" o suba datos de mediciones.`

## Reglas al escribirla

- **Escribe instrucciones, no explicaciones.** "Verifica que cada resultado tenga sus unidades",
  no "es importante que los resultados tengan unidades".
- **Sé específico en el criterio de calidad.** Es la diferencia entre una skill útil y un recordatorio.
- **Corta.** Si pasa de una pantalla, probablemente son dos skills.
- **Pruébala inmediatamente** con un caso real. Si no se activó sola, arregla la `description`
  antes de seguir.

## Al terminar

Muéstrale al usuario la skill completa, dile con qué frase probarla, y **pruébala en ese momento**.
Una skill que nunca se ejecutó no está terminada.
