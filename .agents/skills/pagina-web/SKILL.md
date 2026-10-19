---
name: pagina-web
description: Construye una página web personal en HTML plano, sin instalar nada. Úsala cuando el usuario pida "hazme una página", "quiero un portafolio", "necesito una web para mi proyecto" o "cómo publico esto en internet".
---

# Página web

Una página que se abre en cualquier navegador y se publica gratis. Sin frameworks, sin `npm`, sin
build. Dos archivos: `index.html` y `style.css`.

## Primero el plan, después el código

No escribas una línea de HTML hasta que el usuario apruebe el plan. Pregúntale:

1. **¿Para qué es?** Elige **un** arquetipo y dilo en voz alta:
   - `portafolio` — quién eres, qué sabes hacer, cómo contactarte
   - `proyecto` — qué construiste, cómo funciona, capturas y resultados
   - `cv` — formación, experiencia y habilidades en una sola pantalla
   - `evento` — qué es, cuándo, dónde y un botón para inscribirse
2. **¿Qué secciones?** Máximo cinco. Si pide más, es un sitio, no una página.
3. **¿De dónde sale el contenido?** Busca primero en `AGENTS.md`, `proyectos/` y `entregables/`.

Muéstrale el plan en cinco líneas y espera su aprobación.

## El contenido sale de sus archivos, no de tu imaginación

Esta es la regla que separa una página suya de una página genérica.

- **Textos**: de lo que ya escribió. Si falta algo, **pregúntaselo**. No lo inventes.
- **Datos**: nombre, carrera, proyectos y fechas salen de `AGENTS.md` y de sus carpetas.
- **Colores**: si te da una imagen, un logo o una foto, saca la paleta de ahí. Si no te da nada,
  propón dos o tres opciones y que elija. Nunca decidas el color tú solo.
- Si un dato no está en ningún archivo y él no te lo da, **déjalo fuera y dilo**. Una página con
  tres secciones verdaderas vale más que una con seis inventadas.

## Cómo construirla

Crea `proyectos/<nombre>/` con `index.html` y `style.css`. Nada más.

- HTML semántico: `header`, `main`, `section`, `footer`. Un solo `h1`.
- CSS propio en su archivo. Sin librerías, sin CDN, sin fuentes externas que puedan no cargar.
- **Que se vea bien en el teléfono.** Es donde la va a abrir la gente. Usa `max-width` y unidades
  relativas, y prueba mentalmente a 375px de ancho.
- Contraste suficiente para leerse. Texto de al menos 16px.
- Toda imagen con `alt` que describa lo que se ve.
- **Un solo detalle memorable**: un degradado, una tipografía con carácter, una animación al entrar.
  Uno. Si todo llama la atención, nada la llama.

## Cómo verificar el resultado

Antes de decir que está lista:

1. Ábrela en el navegador y mírala de verdad.
2. Estréchala hasta el ancho de un teléfono. ¿Se rompe algo?
3. Lee los textos. ¿Hay alguno que tú inventaste? Quítalo.
4. ¿Los enlaces van a algún sitio real?

## Cómo publicarla gratis

Cuando el usuario pregunte cómo ponerla en internet, dale estos pasos:

1. Crea un repositorio público en GitHub y sube `index.html` y `style.css`.
2. En el repo: **Settings → Pages → Source: Deploy from a branch → main → / (root)**.
3. En un par de minutos queda en `https://<usuario>.github.io/<repositorio>/`.

Es gratis y no caduca. Si el usuario no tiene cuenta de GitHub, la página igual funciona abriendo
el archivo con doble clic.

## Reglas

- **No inventes contenido.** Ni proyectos, ni fechas, ni experiencia, ni testimonios.
- No instales nada. Si te dan ganas de usar `npm`, es que te fuiste del alcance.
- No publiques nada a nombre del usuario sin que él lo apruebe.
- Una página, un arquetipo. Si pide un sitio de varias páginas, dilo y acota.
