---
name: audit
description: Escanea el sistema, le da un puntaje sobre 100 y propone las tres mejoras que más rinden; con permiso, las aplica. Úsala cuando el usuario diga "/audit", "audita mi sistema", "revisa mi sistema", "¿qué me falta?", "cómo mejoro esto", "qué sigue", después de /conoceme o /conectar, o cada dos semanas.
---

# Audit

Dile al usuario en qué estado está su sistema y **qué hacer a continuación**. Primero escanea y reporta sin tocar nada. Solo edita si el usuario acepta una mejora concreta.

## 1. Escanea

Lee lo que hay. Reporta hechos, no suposiciones: si no leíste un archivo, no hables de él.

`.agents/` y `.opencode/` son carpetas ocultas y las búsquedas por patrón (glob) no las ven. Para revisarlas, lista la carpeta directamente (`ls .agents/skills`) y lee cada `SKILL.md` por su ruta.

| Capa | Puntos | Qué mirar |
|---|---|---|
| Contexto | 25 | `AGENTS.md` existe; cuántos huecos `<...>` quedan; si "En qué estoy trabajando" tiene contenido real; si es específico (carrera, año, materias, formatos). Conserva la línea que ordena revisar `.agents/skills/`. |
| Memoria | 20 | `memory/index.md` existe; cuántas páginas hay en `memory/wiki/` sin contar `ejemplo.md`; páginas huérfanas (no enlazadas desde el índice), por nombre; páginas con `actualizada` de más de 60 días. |
| Capacidades | 20 | Cuántas skills hay en `.agents/skills/` además de las de fábrica (ver `SKILLS.md`); que cada `SKILL.md` tenga `name` igual al nombre de su carpeta y una `description` que diga **cuándo** usarla. |
| Conexiones | 15 | Si `opencode.json` tiene Composio habilitado; si `memory/wiki/conexiones.md` dice qué apps están conectadas. No intentes conectarte para comprobarlo. |
| Espacio de trabajo | 10 | Si hay material propio en `universidad/`, `proyectos/` o `entregables/` además de los README; materias vacías; proyectos sin `NOTAS.md`. |
| Higiene | 10 | Claves, tokens o contraseñas en cualquier archivo (busca `key`, `token`, `secret`, `password`, `sk-`, `ghp_`, sin entrar en `node_modules/` ni `.git/`); datos personales de terceros. **Si encuentras algo, repórtalo sin transcribirlo.** |

Puntaje por capa: completo, la mitad, o cero. Suma el total.

## 2. Mira el uso

Si hay material o memoria, busca tareas que se repitan (por ejemplo, tres resúmenes de clase en `universidad/` o la misma petición en varias páginas de memoria). Si encuentras una, es candidata a skill.

## 3. Reporta

Una tabla y tres acciones. Nada más.

| Capa | Estado | Puntos | Qué encontré |
|---|---|---|---|
| Contexto | ✅ / ⚠️ / ❌ | x/25 | … |
| … | | | |
| **Total** | | **x/100** | |

✅ funciona · ⚠️ funciona pero le falta · ❌ falta o está roto.

Luego, **exactamente tres mejoras**, ordenadas por cuánto suben el puntaje o el valor del sistema. Cada una en una línea, empezando por un verbo, con el archivo que toca. Si hay algo en Higiene, va primero siempre.

Si encontraste una tarea repetida, la tercera mejora es «crear una skill para <tarea>» con `/crear-skill`.

## 4. Ofrece aplicar

Termina con: «¿Aplico alguna? Dime el número». Si acepta:

- Muéstrale en una línea qué vas a cambiar y en qué archivo.
- Haz solo ese cambio.
- Vuelve a puntuar esa capa y dile cuánto subió.

## Reglas

- El escaneo y el reporte no modifican nada.
- Nunca borres material del usuario. Para quitar un secreto, pídele que lo haga él o confirma antes.
- Si la carpeta está recién estrenada, dilo sin dramatismo y propón `/conoceme`.
- Corto: el reporte entero cabe en una pantalla.
