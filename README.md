# Comercializadora de Plásticos Potosina — Catálogo estático con Jekyll

Sitio informativo y catálogo de productos listo para GitHub Pages.

## Cómo usar

1. Crea un repositorio en GitHub y sube todo el contenido de esta carpeta.
2. Settings → Pages → Build and deployment → Source = Deploy from a branch (main /root).
3. Cuando se publique, entra al enlace que GitHub muestre.

### Agregar un producto

Crea un archivo en `_products/` por ejemplo `mi-producto.md` con este formato:

```
---
layout: product
title: "Mi Producto"
order: 3
summary: "Descripción corta."
image: /assets/images/mi-producto.jpg
features:
  - Punto 1
  - Punto 2
specs:
  Propiedad 1: "Valor 1"
  Propiedad 2: "Valor 2"
---

Texto largo de la ficha de producto.
```

### Dominio personalizado (Google Domains)

- En GitHub → Settings → Pages → **Custom domain** = `www.tudominio.com` (se crea archivo `CNAME`).
- En Google Domains (DNS) crea un **CNAME** para `www` apuntando a `tuusuario.github.io`.
- Configura redirección de `tudominio.com` → `www.tudominio.com` en Google Domains.
- Activa **Enforce HTTPS** en GitHub Pages cuando esté disponible.

### SEO básico

- Edita `_config.yml` con `title`, `description`, y más tarde `url` y `baseurl`.
- Incluye `jekyll-seo-tag` y `jekyll-sitemap` compatibles con GitHub Pages.

### Edición desde el navegador

- Puedes editar y crear archivos desde GitHub sin instalar nada.

## Licencia

Libre uso para proyectos informativos.
