---
name: audit
description: Revisa la salud del AIOS y reporta qué le falta. Úsala cuando el usuario pida "corre el audit", "revisa mi sistema", "¿qué me falta?" o después de instalar la plantilla por primera vez.
---

# Audit del AIOS

Revisa este directorio y reporta en qué estado está el sistema del usuario. El objetivo no es
aprobar o reprobar: es decirle **qué hacer a continuación**.

## Qué revisar

Evalúa las cinco capas. Para cada una, asigna un estado y una razón concreta.

### 1. Contexto — `AGENTS.md`

- ¿Existe el archivo?
- ¿Quedan huecos sin rellenar (texto entre `< >`)? Cuenta cuántos.
- ¿La sección "En qué estoy trabajando" tiene contenido real o sigue con el texto de ejemplo?
- ¿Es específico? "Estudio ingeniería" es vago. "Ingeniería Eléctrica, cuarto año, UTP" es útil.

### 2. Memoria — `memory/`

- ¿Existe `memory/index.md`?
- ¿Cuántas páginas hay en `memory/wiki/`, sin contar `ejemplo.md`?
- ¿Todas las páginas están enlazadas desde el índice? Reporta las huérfanas por nombre.
- ¿Hay páginas cuya fecha `actualizada` tenga más de 60 días?

### 3. Skills — `skills/`

- ¿Cuántas skills hay además de las ocho que vienen en la plantilla?
- ¿Cada `SKILL.md` tiene frontmatter con `name` y `description`?
- ¿Las descripciones dicen **cuándo** usar la skill, o solo qué hace? Una descripción sin
  disparadores no se activa nunca.

### 4. Espacio de trabajo — `universidad/`, `proyectos/`, `entregables/`

- ¿El usuario metió material propio, o siguen solo con el `README.md` que trae la plantilla?
- ¿Cuántas materias hay en `universidad/`? ¿Alguna está vacía?
- ¿Los proyectos activos tienen su `NOTAS.md`? Reporta por nombre los que no.
- Un AIOS sin material propio adentro es una carpeta bonita. Si está vacío, dilo.

### 5. Higiene

- ¿Hay contraseñas, tokens o claves de API en algún archivo? Si encuentras algo que lo parezca,
  **repórtalo primero y no lo transcribas.**
- ¿Hay datos personales de terceros?

## Cómo reportar

Una tabla, y debajo la lista de acciones. Nada más.

| Capa | Estado | Qué encontré |
|---|---|---|
| Contexto | ✅ / ⚠️ / ❌ | … |
| Memoria | ✅ / ⚠️ / ❌ | … |
| Skills | ✅ / ⚠️ / ❌ | … |
| Espacio de trabajo | ✅ / ⚠️ / ❌ | … |
| Higiene | ✅ / ⚠️ / ❌ | … |

Criterio: **✅** funciona · **⚠️** funciona pero le falta · **❌** falta o está roto.

Luego, **las tres acciones más útiles**, ordenadas por lo que más mejora el asistente. Ni más ni
menos que tres, cada una en una línea y empezando por un verbo.

Si encontraste algo en Higiene, va de primero siempre, sin importar el resto.

## Reglas

- Reporta lo que **hay**, no lo que debería haber. No inventes archivos que no leíste.
- Si la carpeta está recién estrenada, dilo sin dramatismo y da los primeros tres pasos.
- No modifiques nada. Este audit solo lee y reporta.
