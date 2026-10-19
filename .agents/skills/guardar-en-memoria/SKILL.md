---
name: guardar-en-memoria
description: Escribe una página nueva en la memoria y la enlaza en el índice. Úsala cuando el usuario diga "guarda esto en memoria", "acuérdate de esto", "esto no se te puede olvidar" o cuando aparezca una decisión o un dato estable que valga la pena conservar.
---

# Guardar en memoria

Convierte algo que pasó en una conversación en una página que sobrevive a cerrar la ventana.

## Antes de escribir, decide si vale la pena

No todo va a memoria. Guarda si es **una decisión y su razón**, **un dato estable** (una fecha de
examen, una fórmula, el formato que exige un profesor), **cómo funciona algo que costó entender**, o
**el estado de un proyecto**.

No guardes conversaciones completas, contraseñas, datos personales de terceros, ni cosas que cambian
cada semana. Si dudas, pregúntale al usuario si esto le va a servir dentro de un mes.

## Cómo escribirla

Crea `memory/wiki/<nombre-en-minusculas-con-guiones>.md`:

```markdown
---
titulo: Título en lenguaje natural
tipo: nota | proyecto | decision
creada: AAAA-MM-DD
actualizada: AAAA-MM-DD
---

# Título

## Resumen

Dos o tres líneas. Si alguien solo lee esto, tiene que entender de qué va.

## Detalle

Los hechos, con sus fechas y sus números.
```

Reglas de escritura:

- **Hechos, no narración.** "El parcial de Circuitos II es el 12 de septiembre y cubre hasta el
  capítulo 6" sirve. "Hoy hablamos del parcial" no sirve.
- **Cuando haya una decisión, escribe el porqué.** El dato envejece; la razón sobrevive.
- Escríbela para alguien que no estuvo en la conversación.
- Una página, un tema. Si mezcla dos cosas, son dos páginas.

## Enlázala, o no existe

Dos pasos que no se saltan:

1. Añade la página a la lista de `memory/index.md`.
2. Si se relaciona con otra página existente, enlázalas entre sí con `[enlace](otra-pagina.md)`.

Sin el enlace en el índice, para el agente esa página no existe.

## Al terminar

Dile al usuario **qué guardaste y dónde**, en una línea. Si tuviste que dejar fuera algo por no
estar claro, dilo también.

## Reglas

- Nunca guardes contraseñas, tokens ni claves. Si aparecen en la conversación, avisa y no los
  transcribas.
- No inventes datos para rellenar la página. Lo que no sepas, se queda fuera.
- Si ya existe una página del mismo tema, **actualízala** en vez de crear una nueva. Cambia la
  fecha de `actualizada`.
