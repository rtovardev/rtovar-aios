---
name: brief
description: Resume qué tengo por delante leyendo mi sistema y, si están conectados, mi calendario y mi correo. Úsala cuando el usuario diga "/brief", "qué tengo hoy", "qué tengo pendiente", "por dónde voy", "en qué estaba", "arma mi día" o al empezar una sesión de trabajo.
---

# Brief

Dile al usuario dónde está parado y qué debería atender ahora. Solo lee: nunca envía, crea ni borra nada.

## Qué leer

En este orden, sin pedir permiso:

1. `AGENTS.md`: la sección "En qué estoy trabajando".
2. `memory/index.md` y las páginas con fechas próximas o proyectos activos.
3. `proyectos/*/NOTAS.md`: el estado de cada proyecto.
4. `universidad/`: qué materias hay y si alguna tiene entregas anotadas.
5. **Si hay herramientas de Composio disponibles** (mira `memory/wiki/conexiones.md` o si tienes herramientas `COMPOSIO_*`):
   - Calendario: los eventos de hoy y de los próximos 3 días.
   - Correo: los no leídos de las últimas 24 horas, solo remitente y asunto.
   - GitHub: issues o pull requests abiertos que tenga asignados.

   Usa únicamente acciones de lectura (las que buscan, listan u obtienen). Si una acción manda, crea, actualiza o borra algo, no la uses. Si la conexión falla, sigue sin ella y dilo en una línea.

Si algo no existe, sáltalo sin comentarlo.

## Qué reportar

Corto. Nadie lee un brief de dos pantallas.

**Primero: lo que tiene fecha.** Eventos, entregas, exámenes o compromisos con día, con los días que faltan. Lo que esté a menos de 72 horas va de primero.

**Después: en qué estaba.** Una línea por proyecto activo, con su estado según sus notas.

**Si hay correo conectado:** los mensajes que parezcan pedir respuesta, máximo cinco, una línea cada uno.

**Al final: tres cosas para hoy.** Concretas, empezando por un verbo, ordenadas por lo que más mueve la aguja.

Cierra preguntando por cuál quiere empezar.

## Reglas

- **Solo reporta lo que leíste.** Si no hay fechas anotadas, dilo y sugiere dónde anotarlas. No inventes entregas ni eventos.
- No copies el contenido de los correos, solo remitente y asunto.
- **Si el sistema está casi vacío**, dilo sin rodeos y propón `/conoceme`.
- Si algo lleva semanas sin tocarse, menciónalo una vez.
