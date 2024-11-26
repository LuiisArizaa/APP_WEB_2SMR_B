# Tablas de contenido

Las tablas de contenido nos permiten almacenar los datos de forma ordenada.


Etiquetas para las tablas
------------------------------

El principio y final de una tabla se define con las etiquetas `<table>` y `</table>`. Las filas se engloban con las etiquetas `<tr>` `</tr>` y las columnas se crean mediante las etiquetas `<td>` `</td>` (las etiquetas `<td>` siempre estarán dentro de una fila `<tr>`). Las etiquetas `<th>` `</th>` se utilizan para representar los encabezados. Ejemplo:

```
<table>
  <tr>
    <th>Encabezado 1</th>
    <th>Encabezado 2</th>
    <th>Encabezado 3</th>
  </tr>
  <tr>
    <td>Fila 1, Celda 1</td>
    <td>Fila 1, Celda 2</td>
    <td>Fila 1, Celda 3</td>
  </tr>
  <tr>
    <td>Fila 2, Celda 1</td>
    <td>Fila 2, Celda 2</td>
    <td>Fila 2, Celda 3</td>
  </tr>
</table>
```


Veamos algunas de las etiquetas utilizadas en las tablas:


|Elemento | Descripción |
|---------|--------------|
|`<table>`  |Define la tabla|
|`<caption>`|Título de una tabla|
|`<tr>`    |Representa una fila de celdas en una tabla.|
|`<td>`     |Representa una celda de datos en una tabla.|
|`<th>`     |Representa el encabezado de una tabla.|


Atributos border, align y bgcolor
--------------------------------------

**Para dar estilos a los elementos utilizaremos siempre CSS y no atributos HTML**. No obstante, se van a mencionar estos atributos porque todavía se encuentran presentes en multitud de proyectos online.

Verás que en muchos códigos se le añade un borde a la tabla usando el atributo **_border_**, se alinea el contenido usando el atributo **_align_** o se utiliza el atributo **_bgcolor_** para darle un color de fondo. Sin embargo, estos atributos ya no se suelen utilizar en HTML5.

**¡NO USES LOS SIGUIENTES ATRIBUTOS! Utiliza hojas de estilo CSS**

En el siguiente ejemplo se puede ver cómo se usaba el atributo **_border_** para darle a la tabla un borde dos píxeles.

```
<table border="2">
```


Para modificar la posición de la tabla también se utilizaba el atributo **_align_**. En este caso se usa el valor «center» para posicionar el contenido en el centro. Otros valores podían ser «right» y «left».

```
<table align="center">
```


También se asignaban fondos a las celdas y filas de una tabla con el atributo **_bgcolor_**.

```
<td bgcolor="#77DDEE">
```

En próximas secciones usaremos CSS para dar estilos a nuestras tablas.

Agrupación de celdas
-------------------------

Para agrupar celdas en una sola, también llamado «combinación de celdas», utilizaremos los atributos _**rowspan**_ (para agrupar verticalmente) y _**colspan**_ (para agrupar horizontalmente).


```
<table border="1">
  <caption>Tabla II: Agrupación de celdas en horizontal y verticcal</caption>
  <tr>
    <th>Encabezado 1</th>
    <th>Encabezado 2</th> 
    <th>Encabezado 3</th>
    <th>Encabezado 4</th>
  </tr>
  <tr>
    <td rowspan="2">Campo 1</td>
    <td>Campo 2</td>
    <td>Campo 3</td>
    <td>Campo 4</td>
  </tr>
  <tr>
    <td colspan="2">Campo 6</td>
    <td>Campo 8</td>
  </tr>
  <tr>
    <td>Campo 10</td>
    <td>Campo 11</td>
    <td colspan="2" rowspan="2">Campo 12</td>
  </tr>
  <tr>
    <td>Campo 13</td>
    <td>Campo 14</td>
  </tr>
</table>
```


