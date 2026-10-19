---
name: cerrar-sesion
description: Cierra la sesión de trabajo guardando en memoria lo aprendido, lo decidido y lo pendiente. Úsala cuando el usuario diga "/cerrar-sesion", "cierra la sesión", "terminé por hoy", "guarda lo de hoy", "me voy" o antes de cerrar el agente después de un trabajo largo.
---

# Cerrar sesión

Lo que no se escribe antes de cerrar la ventana se pierde. Esta skill deja la siguiente sesión lista para arrancar.

## Qué hacer

1. **Repasa la conversación** y separa tres cosas:
   - **Decisiones**: qué se decidió y por qué.
   - **Hechos estables**: datos que van a servir después (fechas, requisitos de un profesor, cómo funciona algo).
   - **Pendientes**: lo que quedó a medias, con el siguiente paso concreto.
2. **Actualiza la memoria**:
   - Hechos y decisiones van a la página del tema en `memory/wiki/` (actualiza antes que crear; si no existe, créala y enlázala en `memory/index.md`). Cambia la fecha `actualizada`.
   - El estado de un proyecto va a su `proyectos/<nombre>/NOTAS.md`.
   - Si cambió en qué está trabajando, actualiza esa sección de `AGENTS.md`.
3. **Muéstrale el resumen** en cinco líneas como máximo: qué guardaste, dónde, y el primer pendiente para la próxima vez.

## Reglas

- Hechos, no narración. «La entrega del proyecto de BD2 se movió al 30 de octubre» sí; «hoy hablamos del proyecto» no.
- No guardes la conversación completa, contraseñas ni datos de otras personas.
- Si no hubo nada que valga la pena guardar, dilo y no crees páginas vacías.
- Si una tarea apareció por tercera vez, sugiere `/crear-skill`.
