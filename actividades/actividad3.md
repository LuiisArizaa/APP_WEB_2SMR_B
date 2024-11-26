3\. Crea una tabla de contenido en HTML5
-----------------------------------------------------------------

Imagina que estás creando una página web para un libro en línea y necesitas crear una tabla de contenido para mostrar los capítulos del libro. Debes usar las siguientes etiquetas HTML: `<table>`, `<caption>`, `<tr>`, `<td>`, `<th>`, `<colgroup>`, `<col>`, `<tbody>`, `<thead>`, `<tfoot>` y los atributos `rowspan` y `colspan` según sea necesario.

*   Crea una tabla `<table>` que contendrá la tabla de contenido del libro.
*   Agrega una fila de encabezado `<thead>` a la tabla con una fila `<tr>`.
*   En la fila de encabezado, agrega celdas de encabezado `<th>` para las siguientes columnas: Capítulo, Título del Capítulo y Páginas.
*   Utiliza el atributo `colspan` para combinar las tres celdas de encabezado en una sola celda de encabezado que tenga el texto «Contenido del Libro».
*   Ahora, agrega tres filas `<tr>` en la sección del cuerpo `<tbody>` de la tabla para representar los primeros tres capítulos del libro.
*   Dentro de cada fila, agrega una celda de datos `<td>` para cada columna (Capítulo, Título del Capítulo y Páginas). Llena estas celdas con información de ejemplo para los primeros tres capítulos del libro.
*   Utiliza el atributo `rowspan` para combinar las celdas de datos de los capítulos en una sola celda para cada capítulo. Esto indicará cuántas filas ocupa cada capítulo.
*   Luego, agrega una fila `<tr>` adicional para representar el cuarto capítulo del libro. En este caso, el cuarto capítulo debería ocupar solo una fila.
*   Completa la tabla agregando más filas y celdas de datos para representar más capítulos del libro, manteniendo la estructura de la tabla de contenido.

