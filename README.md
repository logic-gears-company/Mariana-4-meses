# Mariana · 4 meses

Experiencia romántica de una sola página, 100% estática (HTML + CSS + JS, sin backend ni build step) — lista para Cloudflare Pages o Cloudflare Workers + Assets.

## Personalización

### Fotos
El diseño usa dos fotos:
- `public/photos/mariana-01.jpg` — foto principal (hero + primer cuadro de la galería)
- `public/photos/mariana-03.jpg` — segunda foto de la galería

Puedes reemplazar cualquiera de las dos manteniendo el mismo nombre de archivo. Si en algún momento quieres usar `mariana-02.jpg` en su lugar, busca `mariana-03.jpg` dentro de `public/index.html` (aparece dos veces) y cámbialo por `mariana-02.jpg`.

Si un archivo de foto falta al momento del deploy, ese recuadro muestra automáticamente un aviso elegante en vez de romperse.

### Música
Añade una copia legal de tu canción en:
- `public/music/beatles.mp3`

No se incluye una copia de música de The Beatles en este paquete.

### Deploy

```bash
npx wrangler deploy
```

No necesita build command. No necesita `npm install`. No hay ninguna llamada de red obligatoria en el arranque: la animación de apertura y todas las transiciones están hechas con CSS y la Web Animations API nativa del navegador, así que la página nunca se queda "atascada" si la fuente de Google Fonts tarda o si un bloqueador de contenido interfiere.
