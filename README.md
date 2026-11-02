# Visor 3D de PCB (STEP)

Este repositorio muestra `modelo.step` directamente en una página web mediante Three.js y `occt-import-js` (WebAssembly/OpenCascade). No es necesario convertir el STEP a GLB antes de publicarlo.

## Archivos

- `index.html`: página y visor 3D interactivo.
- `modelo.step`: modelo CAD original exportado desde EasyEDA.

## Publicar en GitHub Pages

1. Crea un repositorio en GitHub.
2. Sube `index.html`, `modelo.step` y `README.md` a la raíz del repositorio.
3. Entra a **Settings → Pages**.
4. En **Build and deployment**, elige **Deploy from a branch**.
5. Selecciona la rama `main` y la carpeta `/ (root)`, y guarda.
6. Cuando termine el despliegue, abre la URL que GitHub muestra en esa sección.

## Controles

- Arrastrar con el botón izquierdo: girar.
- Rueda del mouse: acercar/alejar.
- Arrastrar con botón derecho: desplazar.

## Notas

- La página procesa el STEP en el navegador usando WebAssembly. La primera carga descarga el motor CAD y puede tardar; el tiempo de procesamiento depende del dispositivo y de la complejidad del modelo.
- El visor usa CDN para cargar Three.js y `occt-import-js`; requiere conexión a Internet.
- El archivo STEP original se mantiene sin modificar. La triangulación ocurre al abrir la página.
