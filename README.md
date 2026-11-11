# Documento 1 — versión web

Capítulo 2, «Transportador». Aventura narrativa hecha en Unity 6 (URP 2D, WebGL 2).
Se juega con ratón y teclado; mejor con auriculares.

Esta carpeta es el sitio ya compilado: `index.html` está en la raíz y no hay que compilar nada.

## Publicar en Cloudflare Pages

- Framework preset: **None**
- Build command: *(vacío)*
- Build output directory: **/**

Los archivos de `Build/` van comprimidos con Brotli. El cargador de Unity los descomprime él
mismo si el servidor no manda `Content-Encoding: br`, así que funciona en cualquier hosting
estático sin configurar nada. El archivo más grande ocupa unos 17 MB (Cloudflare admite hasta 25 MiB).

## Actualizar

En el proyecto: `./make.sh web`. Después hay que copiar aquí el contenido de
`Documento1/Builds/Web/` y subirlo.

## Licencias

Tipografía Spectral: SIL Open Font License (`TemplateData/Spectral-OFL.txt`).
