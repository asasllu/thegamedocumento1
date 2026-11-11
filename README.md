# Documento 1 — versión web

Aventura gráfica narrativa hecha en Unity 6 (URP 2D, WebGL 2): Londres, 2020, bajo la Gran Pantalla.
La historia completa: prólogo, nueve capítulos, epílogo y cuatro finales («Segunda edición», «Iteración 65»,
«Escéptico» y el final verdadero). Se juega con ratón y teclado; mejor con auriculares.
La partida se guarda sola en el navegador; el menú principal tiene «Continuar», «Nueva partida» y «Capítulos».

Esta carpeta es el sitio ya compilado: `index.html` está en la raíz y no hay que compilar nada.

## Publicar en Cloudflare Pages

- Framework preset: **None**
- Build command: *(vacío)*
- Build output directory: **/**

Los datos van en un archivo por escena (`level*.unityweb`, `sharedassets*.unityweb`): al abrir el juego sólo se
descarga lo del menú y el primer capítulo, y el resto llega en segundo plano. Van comprimidos con Brotli y el
cargador de Unity los descomprime él mismo si el servidor no manda `Content-Encoding: br`, así que funciona en
cualquier hosting estático sin configurar nada. Ningún archivo pasa de 8 MB (Cloudflare admite hasta 25 MiB).

## Actualizar

En el proyecto: `./make.sh web` y después `./publish_web.sh "mensaje"`.

## Licencias

- Música: Ludwig van Beethoven, Sonata n.º 14 «Claro de luna», I. Adagio sostenuto; interpretación de Paul Pitman
  para Musopen (dominio público).
- Tipografías: Spectral (`TemplateData/Spectral-OFL.txt`), Inter y Roboto Mono, con licencia SIL Open Font License.
- Captura de movimiento: CMU Graphics Lab Motion Capture Database.
