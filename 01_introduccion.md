# Lenguaje de marcas HTML

El lenguaje de marcas **HTML** (_HyperText Markup Language_) es el lenguaje de marcado estándar utilizado para crear páginas web. Este lenguaje proporciona la estructura y el contenido de una página web.

HTML utiliza etiquetas para marcar diferentes partes del contenido, como encabezados, párrafos, enlaces, imágenes, tablas, formularios, entre otros. Estas etiquetas permiten a los navegadores web **interpretar y renderizar correctamente el contenido de la página.**

El lenguaje de marcas HTML es un estándar reconocido en todo el mundo y sus normas están definidas en la página web del organismo [**W3C**](http://w3c.es/) **(World Wide Web Consortium)** y en la página oficial del grupo de trabajo **[WHATWG](https://whatwg.org/) (Web Hypertext Application Technology Working Group).** 

### Breve historia HTML

HTML fue desarrollado por **[Tim Berners-Lee](https://es.wikipedia.org/wiki/Tim_Berners-Lee)** en **1991** como parte del proyecto World Wide Web en el **CERN** (**Consejo Europeo para la Investigación Nuclear**). A lo largo de los años, HTML ha evolucionado con nuevas versiones y características para adaptarse a las necesidades cambiantes de la web.

La última versión estable es HTML5, que ofrece mejoras en multimedia, interactividad y accesibilidad. HTML ha sido **fundamental en el crecimiento y la expansión de Internet**, permitiendo la creación de contenido digital accesible a nivel mundial.

En el este vídeo puedes conocer de forma breve la **historia de HTML**: **[ver vídeo](https://www.youtube.com/embed/EEttUcYhv30)**


### Documentación oficial y páginas de referencia de HTML

La documentación oficial y las páginas de referencia más importantes para HTML son mantenidas principalmente por el W3C (World Wide Web Consortium) y WHATWG (Web Hypertext Application Technology Working Group). Veamos las principales fuentes:

| Fuente | Enlace | Descripcion |
|--------|--------|-------------|
| WHATWG (Web Hypertext Application Technology Working Group)| [HTML Living Standard](https://html.spec.whatwg.org/) |Esta es la versión continuamente actualizada del estándar HTML mantenida por WHATWG|
|MDN Web Docs (Mozilla Developer Network)|[MDN HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)|Una referencia con documentación, tutoriales y ejemplos prácticos|
|Can I use|[Can I use](https://caniuse.com/)|Información sobre la compatibilidad de características HTML en diferentes navegadores|
|HTML5 Doctor|[HTML5 Doctor](https://html5doctor.com/)|Ofrece artículos y recursos sobre las características de HTML5, con ejemplos prácticos y explicaciones|
|W3Schools|[W3Schools HTML](https://www.w3schools.com/html/)|Tutoriales interactivos y referencias fáciles de seguir para aprender y practicar HTML|

## Etiquetas y atributos en HTML

Una **etiqueta** es un elemento que define la estructura y el contenido de una página web. Las etiquetas se utilizan para marcar o envolver diferentes partes del contenido, como textos, imágenes, enlaces, listas, entre otros elementos. Por ejemplo, `<p>` define un párrafo y `<img>` define una imagen.

Por otro lado, un **atributo** proporciona información adicional sobre una etiqueta y suele especificarse dentro de la etiqueta de apertura. Los atributos modifican el comportamiento o la apariencia de las etiquetas y pueden ser obligatorios u opcionales dependiendo del contexto.

**Ejemplos:**

1\. En la etiqueta `<html>`, el atributo `lang` especifica el idioma del documento HTML.

```
<html lang="es">
```


2\. En la etiqueta `<meta>`, el atributo `charset` especifica la codificación de caracteres del documento HTML. Utilizamos `charset="UTF-8"`, ya que es la codificación compatible con la mayoría de los caracteres de diferentes idiomas y nos permite una correcta visualización del contenido en distintos navegadores. Ver más información sobre [sistemas de codificación](https://www.eniun.com/representacion-comunicacion-informacion/#31_Sistemas_de_codificacion).

```
<meta charset="UTF-8">
```


3\. En la etiqueta `<meta>`, el atributo `name` especifica metadatos adicionales del documento HTML, como el título o la descripción, lo cual es importante para el SEO y la manera en que los motores de búsqueda indexan una página.

```
<meta name="title" content="Título de la web"> 
<meta name="description" content="Descripción de la web">
```


## Comentarios

Los comentarios se escriben entre los caracteres que se muestran en el siguiente ejemplo:

```
<!-- Esto es un comentario dentro de un documento HTML -->
<!--
 /$   /$ /$$$$ /$      /$ /$      
| $  | $|__  $__/| $$    /$$| $      
| $  | $   | $   | $$  /$$| $      
| $$$$   | $   | $ $/$ $| $      
| $__  $   | $   | $  $$| $| $      
| $  | $   | $   | $\  $ | $| $      
| $  | $   | $   | $ \/  | $| $$$$
|__/  |__/   |__/   |__/     |__/|________/
 -->                                         
<!--¿Te están entrando ganas de hacer ASCII Art? Puedes hacerlo en: http://patorjk.com/software/taag/#p=display&f=Big%20Money-ne&t=ENIUN -->
```


## Nuestro primer código html

Crear un archivo HTML es el primer paso para desarrollar una página web básica. Para hacerlo, no es necesario un software especializado, aunque es altamente recomendable utilizar un editor de código para facilitar el proceso de escritura y evitar errores. Nosotros utilizaremos **Visual Studio Code**.

Para trabajar de manera más cómoda vamos a instalar las siguientes extensiones en **Visual Studio Code**:

* [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer). Live server en Visual Studio Code es una herramienta que nos permite lanzar un servidor de desarrollo local para previsualizar en el navegador lo que estamos escribiendo en nuestro editor de código.

* [**Emmet**](https://docs.emmet.io/cheat-sheet/). Las abreviaciones Emmet son una herramienta para aumentar la productividad y eficiencia en el desarrollo web. Emmet, anteriormente conocido como Zen Coding, nos permite escribir menos y lograr más al expandir abreviaciones en código HTML y CSS completos.

Vamos ahora a crear un archivo con extensión html (.html) en el editor de texto. Vamos a hacer click con el botón derecho y marcar la opcion **_Open with Live Server_**. Se abrirá una pestaña nueva en nuestro navegador con el dominio _http://127.0.0.1:5500/nombre-del-archivo.html_

Vamos a ver ahora que cada vez que escribamos una linea o una etiqueta en el archivo abierto de nuestro editor de texto, se actualizará automáticamente y se visualizará en la pestaña de nuestro navegador.
    
Para hacer la prueba vamos a copiar y pegar el siguiente código en el archivo que nos hemos creado y vamos visualizalo en la pestaña que se ha abierto en el navegador.

```
<!DOCTYPE html>
<html lang="es">  
<head>    
    <title>Título de la WEB</title>    
    <meta charset="UTF-8">
    <meta name="title" content="Título de la WEB">
    <meta name="description" content="Descripción de la WEB">    
    <link href="estilos.css" rel="stylesheet">
    <style>
        header{background-color:yellow;} /* Código CSS */
    </style> 
    <script src="script.js"></script>  
    <script type="text/javascript">
        /* Código JS */
    </script> 
</head> 
<body>
    ¡Hola Mundo!
    <!-- Añade tu código HTML aquí -->
</body>
</html>
```

Vamos a modificar el cuerpo de nuestra web. Para ello usaremos la abreviación `lorem` y generaremos texto «lorem ipsum». Para ello simplemente debemos escribir `lorem` en el editor.
¡Mira como se va actualizando automáticamente el navegador!


**Explicación del código:**

*   `<!DOCTYPE html>`: Declara que el documento está escrito en HTML5.
*   `<html lang="es">`: Indica el inicio del documento HTML y establece el idioma del contenido como español, lo que ayuda con la accesibilidad y el SEO.
*   `<head>`: Contiene metadatos sobre el documento.
*   `<title>Título de la WEB</title>`: Define el título de la página web, que aparece en la pestaña del navegador.
*   `<meta charset="UTF-8">`: Especifica la codificación de caracteres. En nuestro caso usamos UTF-8 porque es una codificación de caracteres que permite representar prácticamente todos los caracteres de los distintos lenguajes del mundo de manera universal.
*   `<meta name="title" content="Título de la WEB">`: Proporciona información sobre el título del documento.
*   `<meta name="description" content="Descripción de la WEB">`: Proporciona una descripción del contenido de la página.
*   `<link href="estilos.css" rel="stylesheet">`: Enlaza un archivo CSS externo para dar estilo a la página.
*   `<style> header {background-color: yellow;} </style>`: Incluye un bloque de estilo CSS que establece el color de fondo del elemento `header` como amarillo.
*   `<script src="script.js"></script>`: Enlaza un archivo JavaScript externo.
*   `<script type="text/javascript"> /* Código JS */ </script>`: Incluye un bloque de código JavaScript interno.
*   `<body>`: Contiene el contenido visible de la página web.
*   `¡Hola Mundo!`: Texto que se mostrará en la página web.
*   `<!-- Añade tu código HTML aquí -->`: Un comentario HTML que no se mostrará en la página web.

## Reglas y normas HTML5

Con el aumento de la complejidad y la interactividad en los sitios web, es más importante que nunca adherirse a las mejores prácticas de HTML5 para ofrecer una experiencia de usuario óptima y eficiente. Veamos las reglas y normas que nos ayudan a seguir buenas prácticas en la implementación de código HTML:

1.  **Estructura básica:** Todo documento HTML5 debe tener una estructura básica que incluya las etiquetas `<!DOCTYPE html>` `<html>`, `<head>`, y `<body>`. La etiqueta `<html>` es el elemento raíz y debe contener todas las demás etiquetas.
2.  **Etiquetas en mayúsculas o minúsculas:** Las etiquetas HTML no distinguen entre mayúsculas y minúsculas. Por lo tanto, `<HTML>` y `<html>` son equivalentes. Se recomienda seguir siempre la misma sintaxis, preferiblemente letras en minúsculas.
3.  **Caracteres especiales:** Algunos caracteres especiales, como `<`, `>`, `&`, `"`, y `'`, tienen significados especiales en HTML. Para incluir estos caracteres en tu código, puedes usar entidades HTML (`&lt;` representa el símbolo `<`), su código decimal (`&#60;` representa el símbolo `<`) o hexadecimal. 
4.  **Código con tabulados y sangrías:** El código HTML indentado con tabulados facilita la lectura y su comprensión. Además, puede ayudar a evitar errores, ya que facilita la identificación de los elementos HTML. Por ello, cuando escribimos código HTML utilizamos la tabulación para entender mejor la estructura de etiquetas. Sin embargo, hay que tener en cuenta también que la **velocidad de carga** es uno de los factores más influyentes en la experiencia que reciben los usuarios. Por ello, para **reducir el tamaño de los ficheros HTML** hay que evitar los tabulados, los espacios en blanco y los comentarios innecesarios. Una vez implementado nuestro código, se puede minificar mediante herramientas específicas.
5.  **Los saltos de línea y los espacios no tienen ningún efecto en el código HTML:** Los navegadores web ignoran los saltos de línea y los tabuladores en el código HTML contenido entre las etiquetas `<body></body>`. Para escribir espacios en blanco podemos usar `&nbsp;` y para escribir saltos de línea la etiqueta `<br>`.
6.  **Uso de comillas:** Aunque HTML5 permite el uso de comillas simples (`'`) alrededor de los valores de los atributos, es una buena práctica utilizar comillas dobles (`"`) para que el código sea más consistente. `<a href="pagina.html">Enlace</a>`
7.  **Pruebas en diferentes navegadores:** Prueba tu sitio web en diferentes navegadores y dispositivos para garantizar que se vea y funcione correctamente en todas partes.

