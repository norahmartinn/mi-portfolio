# norah · portfolio

Portfolio personal de Norah Martín — economista y programadora.

Sitio estático, un único archivo HTML autocontenido (todas las imágenes y estilos embebidos).

## Publicar en GitHub Pages

### Opción 1 — desde la web de GitHub (más fácil)

1. Entra en [github.com](https://github.com) y crea un repositorio nuevo.
   - Nombre sugerido: `portfolio` (o `norahmartinn.github.io` si quieres URL sin subcarpeta).
   - Márcalo como **Public**.
2. En la página del repositorio recién creado, haz click en **"uploading an existing file"**.
3. Arrastra los tres archivos de esta carpeta: `index.html`, `.nojekyll` y `README.md`.
4. Dale a **Commit changes**.
5. Ve a **Settings → Pages** (en la barra lateral izquierda).
6. En **Source**, selecciona la rama `main` y la carpeta `/ (root)`. Guarda.
7. Espera 1–2 minutos y tu portfolio estará en:
   - `https://norahmartinn.github.io/portfolio/` (si llamaste al repo `portfolio`)
   - `https://norahmartinn.github.io/` (si lo llamaste `norahmartinn.github.io`)

> **Si no aparece `.nojekyll`** al arrastrar (GitHub a veces ignora archivos ocultos):
> dentro del repo haz click en **Add file → Create new file**, escribe `.nojekyll` como nombre y dale a commit. No necesita contenido.

### Opción 2 — desde la terminal (si usas git)

```bash
cd portfolio-site
git init
git add .
git commit -m "Primera versión del portfolio"
git branch -M main
git remote add origin https://github.com/norahmartinn/portfolio.git
git push -u origin main
```

Luego activa Pages en Settings → Pages → Source: main / root.

## Editar el portfolio

Todo el contenido vive dentro del único archivo `index.html`, en el bloque
`<script type="text/babel">`. Para cambiar textos o proyectos:

- **Proyectos**: array `PROJECTS` (título, subtítulo, resumen, hitos, URL, tags).
- **Datos de contacto**: objeto `NORAH` arriba del script (email, LinkedIn, GitHub).
- **Paleta de colores**: variables CSS en `:root` dentro de `<style>`:
  - `--bg` (cobalto de fondo)
  - `--fg` (blanco)
  - `--accent` (tangerine naranja)

## Dominio personalizado

Si más adelante quieres usar un dominio propio (tipo `norahmartin.com`), añade
un fichero `CNAME` en la raíz del repo con el dominio dentro y configura los
registros DNS según la guía de GitHub Pages.

---

© 2026 Norah Martín
