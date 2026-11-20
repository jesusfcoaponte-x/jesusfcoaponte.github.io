# Grilla dinámica de programación radial

Este ejemplo muestra el flujo que se instalará en el Home:

1. GitHub Pages publica `data/programacion.csv`.
2. `js/programacion.js` lee el CSV al abrir la página.
3. La página dibuja automáticamente la grilla semanal.

## Probarlo en GitHub Pages

Sube la carpeta y conserva esta estructura:

- `index.html`
- `css/programacion.css`
- `js/programacion.js`
- `data/programacion.csv`

Activa GitHub Pages en el repositorio. La página consultará el CSV cada vez que se cargue.

## Cambiar la programación

Edita únicamente `data/programacion.csv`. Cada fila representa una emisión en un día.

Columnas:
- `programa`: nombre del programa.
- `dia`: Lunes, Martes, Miércoles, Jueves, Viernes, Sábado o Domingo.
- `inicio`: hora `HH:MM`.
- `fin`: hora `HH:MM`; admite `24:00` como final del día.
- `color`: color hexadecimal, por ejemplo `#5B9BD5`.
- `locutor` y `descripcion`: opcionales.

Si un programa termina después de medianoche, por ejemplo `21:00` a `01:00`, la página lo divide automáticamente entre el día de inicio y el siguiente.

## Integrarlo en un Home existente

Este ZIP es una demostración independiente para probar el mecanismo. En el Home definitivo se conserva el diseño de la web y se reemplaza únicamente el espacio ocupado por la imagen de programación por el bloque HTML de la grilla. También se enlazan el CSS y el JS desde el Home. La ruta del CSV debe ajustarse a su ubicación real dentro del repositorio.

No hay panel de administración ni un generador que tengas que abrir: el código de visualización queda instalado una sola vez.
