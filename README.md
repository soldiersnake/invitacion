# Invitación de Casamiento

Landing page de invitación para casamientos, en un solo archivo `index.html`, sin npm ni build. Pensada como plantilla reutilizable: cada pedido nuevo se arma cambiando un único bloque de configuración.

## Tecnologías

- **HTML5** — única página: `index.html`
- **JavaScript (vanilla)** — arma la página desde el objeto `INVITATION`
- **Tailwind CSS** — vía Play CDN (`cdn.tailwindcss.com`), sin build ni npm
- **Google Fonts** — Cormorant Garamond (títulos) y Outfit (texto)

## Cómo verla

Abrí `index.html` en el navegador. No hace falta instalar nada (requiere internet por el CDN de Tailwind y las fuentes).

## Estructura

```
index.html      página completa + objeto de configuración INVITATION
images/         fotos del casamiento (hero.jpg, gallery-1.jpg, ...)
music/          canción de fondo (mp3, wav, ogg...)
```

## Uso por pedido

Todo lo personalizable está en el objeto `INVITATION` dentro de `index.html`:

- `couple` — nombres de los novios
- `copy` — todos los textos de la página
- `event` — fecha y hora
- `venue` — nombre, dirección y búsqueda de Google Maps
- `images` — rutas de fotos (deben estar en `images/`)
- `music.src` — canción de fondo; si queda vacío, se oculta el reproductor
- `rsvp.whatsapp` — número con código de país, sin `+` ni espacios

Si las fotos se llaman `hero.jpg`, `gallery-1.jpg`... no hay que tocar el código. La canción va en `music/` y su ruta exacta (con extensión, ej. `music/vals.mp3`) se setea en `INVITATION.music.src`. Detalles en `images/LEEME.txt` y `music/LEEME.txt`.

## Secciones

Portada con foto → texto de invitación → cuándo y dónde (con mapa) → galería → confirmación por WhatsApp → pie. Incluye botón flotante ♪ para el vals de fondo y diseño responsivo (mobile-first).

## Contacto

- Email: [mariano.maciasgandulfo@gmail.com](mailto:mariano.maciasgandulfo@gmail.com)
