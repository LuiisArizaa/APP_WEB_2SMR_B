# Contenido incrustado
El contenido incrustado se utiliza para mostrar recursos externos como, por ejemplo, mapas, previsiones meteorológicas, fórmulas matemáticas, vídeos y audios, entre otros. Este método permite utilizar un servicio o interfaz de terceros.

Etiquetas para incrustar contenido
---------------------------------------

Algunas de las etiquetas más importantes para incrustar contenido son las siguientes:

| Elemento | Descripcion |
|----------|-------------|
|``<img>``|Representa una imagen|
|``<iframe>``|Representa un contexto anidado de navegación, es decir, un documento HTML embebido|
|``<embed>``|Representa un punto de integración para una aplicación o contenido interactivo externo que por lo general no es HTML|
|``<object>``|Representa un recurso externo, que será tratado como una imagen, un sub-documento HTML o un recurso externo a ser procesado por un plugin|
|``<video>``|Representa un vídeo|
|``<audio>``|Representa un sonido|
|``<source>``|Permite a autores especificar recursos multimedia alternativos para los elementos multimedia como  <video> o <audio>|
|``<canvas>``|Representa un área de mapa de bits en el que se pueden utilizar scripts para renderizar gráficos|
|``<svg>``|Define una imagen vectorial embebida|

## Ejemplo

```
<!DOCTYPE html>
<html>
<head>
  <title>Ejemplo de Incrustación de Contenido</title>
</head>
<body>
  <h1>Ejemplo de Incrustación de Contenido</h1>

  <!-- Incrustación de una imagen -->
  <img src="imagen.jpg" alt="Imagen">

  <!-- Incrustación de un video -->
  <video src="video.mp4" controls></video>

  <!-- Incrustación de un audio -->
  <audio src="audio.mp3" controls></audio>

  <!-- Incrustación de una página web externa -->
  <iframe src="https://www.ejemplo.com"></iframe>

  <!-- Incrustación de contenido externo utilizando plugins -->
  <embed src="contenido.swf">

  <!-- Incrustación de contenido multimedia o plugins -->
  <object data="contenido.swf" type="application/x-shockwave-flash"></object>

  <!-- Incrustación de un lienzo para dibujar gráficos -->
  <canvas id="miCanvas" width="200" height="200"></canvas>

  <!-- Incrustación de gráficos vectoriales escalables -->
  <svg width="400" height="180">
    <rect x="50" y="20" width="300" height="100" style="fill:blue" />
  </svg>
</body>
</html>

```


Etiqueta `img`
-------------------

Los atributos más comunes en las etiquetas de imagen HTML son:

*   **src**: especifica la ruta o URL de la imagen.
*   **alt**: proporciona texto alternativo que se muestra si la imagen no se puede cargar.
*   **title**: proporciona texto descriptivo que se muestra al pasar el cursor sobre la imagen.
*   **width**: especifica el ancho de la imagen en píxeles o como un porcentaje del ancho disponible.
*   **height**: especifica la altura de la imagen en píxeles o como un porcentaje de la altura disponible.

Además, puedes ver en proyectos más antiguos el uso de los siguientes atributos:

*   **border**: especifica el ancho del borde alrededor de la imagen. **Ya no se utiliza, mejor usar estilos CSS.**
*   **align**: especifica la alineación de la imagen con respecto al texto circundante. Valores: left | right| middle| top| bottom. **Ya no se utiliza, mejor usar estilos CSS.**

En el siguiente ejemplo, la imagen se carga desde el archivo «imagen.jpg». Si la imagen no se puede cargar, se mostrará el texto «Descripción de la imagen». Al pasar el cursor sobre la imagen, se mostrará el texto «Título de la imagen». La imagen tendrá un ancho de 300 píxeles y una altura de 200 píxeles.

```
<img src="imagen.jpg" alt="Descripción de la imagen" title="Título de la imagen" width="300" height="200">
```


*   Las imágenes pueden insertarse en distintos formatos: .jpg, .png, .svg…
*   Para insertar una imagen en formato SVG se puede utilizar la etiqueta `<img>`. 
*   Cuando no se indica el ancho o alto de una imagen (ni en HTML ni en CSS) se incrusta con su tamaño por defecto.

Las **imágenes SVG** funcionan muy bien para logotipos, iconos, gráficos y diagramas. No pierden su calidad al ampliarlas o cambiarlas de tamaño. Como los archivos SVG son sólo código, tienen un tamaño reducido y se pueden comprimir aún más mediante programas específicos.

Incrustar videos de YouTube
--------------------------------

1.  Ve al vídeo o a la lista de reproducción de YouTube que quieras insertar.
2.  Haz clic en **COMPARTIR** ![""](https://lh3.googleusercontent.com/rrvxraXG0vl4fbT5P2ErhOnccyvBqYgsX-nb_-ixD232i-ANhm7OYD0Dtdi_7AqghS4=w36).
3.  En la lista de opciones que se muestra, haz clic en **Insertar**.
4.  Copia el código HTML del cuadro que aparece.

Incrustar un mapa de Google
--------------------------------

1.  Accede a las indicaciones, al mapa o a la imagen de Street View que quieras insertar.
2.  En la parte superior izquierda, haz **clic en Menú** ![Menú](https://storage.googleapis.com/support-kms-prod/CD148BFC3EE3B5328DAFE08E2B6AA95B73B7).
3.  Haz clic en **Compartir o insertar el mapa**.
4.  Haz clic en **Insertar un mapa**.
5.  A la izquierda del cuadro de texto, haz **clic en el icono de la flecha hacia abajo** ![Flecha hacia abajo](https://lh3.googleusercontent.com/7acH9pM1qZl0MEFmPRkOPeuNk48-E7Wbn08-h9yfGXbkMTKHY0kOPqurH20N2jHFwZY=w36-h36) para elegir el tamaño que desees.
6.  Copia el texto en el cuadro y pégalo en el HTML de tu sitio web o blog.

En el siguiente código se muestra cómo incrustar una imagen, un mapa de Google Maps y un vídeo de Youtube.

```
<h3>Etiqueta img</h3>
<img src="https://www.eniun.com/wp-content/uploads/eniun-icon-user-experience.svg"
     alt="Usabilidad">

<h3>Etiqueta iframe</h3>
<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d154214.5103364689!2d-0.5427351669515812!3d38.35795447718404!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0xd6235da3b9dab4b%3A0x1d7da872ac0b81e3!2sAlicante+(Alacant)%2C+Alicante%2C+Espa%C3%B1a!5e1!3m2!1ses!2sus!4v1564299065614!5m2!1ses!2sus" width="600" height="400" frameborder="0" style="border:0" allowfullscreen></iframe>

<h3>Etiqueta iframe</h3>
<iframe width="600" height="400" src="https://www.youtube.com/embed/coy5h2w5xUg" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

```


