---
name: mejorar
description: Propone la siguiente mejora concreta para tu AIOS, mirando cómo lo has estado usando. Úsala cuando el usuario diga "cómo mejoro esto", "qué le falta a mi sistema", "corre el mejorar", "hazlo mejor" o cada cierto tiempo para no estancarse.
---

# Mejorar

El `audit` te dice **qué está roto**. Esta te dice **qué vale la pena hacer después**. No repitas su
trabajo: aquí no hay semáforo ni higiene, hay una propuesta.

## Busca oportunidades, no errores

Revisa el espacio buscando estas cuatro señales, en este orden:

1. **Algo que se repite.** Mira `memory/wiki/` y las carpetas de trabajo: ¿hay una tarea que aparece
   tres o más veces? Ese es el mejor candidato a skill nueva. Es la señal más valiosa de todas.
2. **Contexto que envejeció.** ¿La sección "En qué estoy trabajando" de `AGENTS.md` habla de algo que
   ya terminó? ¿Hay páginas de memoria de hace más de dos meses que ya no aplican?
3. **Material que no está aprovechado.** ¿Hay PDF o apuntes en `universidad/` que nunca se usaron
   para nada? ¿Proyectos sin `NOTAS.md`?
4. **Skills que no se usan.** ¿Alguna de las skills existentes nunca aparece en el trabajo del
   usuario? Puede ser que su `description` no tenga los disparadores correctos.

## Propón una sola cosa

Este es el punto de la skill. **Elige la mejora de mayor impacto y preséntala sola**, con:

- **Qué proponés** en una frase.
- **Por qué ahora**: la evidencia que encontraste, citando el archivo o la carpeta.
- **Qué gana**: el tiempo o el esfuerzo que le ahorra, concreto.
- **El primer paso**, que debe caber en diez minutos.

Después menciona en una línea las otras dos oportunidades que viste, sin desarrollarlas. Si el
usuario quiere otra, que la pida.

## Si la propuesta es una skill nueva

Es el caso más común. No la escribas de una: dile el nombre que tendría, con qué frase la
dispararía, y ofrécele pasar a `crear-skill`. Ahí es donde se escribe bien.

## Si el sistema todavía está vacío

No inventes oportunidades para llenar el reporte. Dile la verdad: que lleva poco uso, que la mejora
es meterle material y trabajar con él una semana, y que vuelva a correr esto después. **Un consejo
inventado es peor que ninguno.**

## Reglas

- **Una propuesta principal.** No listas de diez. Si propones todo, no propones nada.
- Solo evidencia real: cita el archivo o la carpeta donde la viste. Si no puedes citarla, no la digas.
- No dupliques el `audit`. Los huecos y la higiene no son tu trabajo.
- No modifiques nada. Esta skill lee y propone; ejecutar lo decide el usuario.
