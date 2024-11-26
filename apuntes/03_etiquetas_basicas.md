
# Tipos de etiquetas

##  Etiquetas básicas

Al escribir código HTML existen algunas características, como pueden ser los saltos de línea, las negritas, múltiples espacios seguidos, cursivas o sangrías que tienen que indicarse expresamente utilizando diferentes etiquetas HTML.

Para poner un ejemplo práctico vamos a utilizar un texto de [Wikipedia](http://es.wikipedia.org/wiki/Fenomenolog%C3%ADa_del_esp%C3%ADritu) sobre la interesante y amena obra _'Fenomenología del espíritu'_ de nuestro amigo Hegel de 1807, (fantástica como lectura ligera de noche).

Así, el siguiente código HTML, escrito en cualquier editor HTML:

```
Título: Fenomenología del espíritu

Subtítulo: Contenido de la obra  

La Idea en su ser en y para sí misma, al regresar del gran círculo en que, a partir de su ser en sí, recorrió los sucesivos momentos de su alteridad, constituye el objeto de la filosofía del espíritu.
```

En el navegador se visualiza todo seguido (sin ningún salto de línea, ni sangría):

```
Título: Fenomenología del espíritu Subtítulo: Contenido de la obra La Idea en su ser en y para sí misma, al regresar del gran círculo en que, a partir de su ser en sí, recorrió los sucesivos momentos de su alteridad, constituye el objeto de la filosofía del espíritu.
```

Para poder visualizarlo añadiendo negritas, saltos de página, párrafos y sangrías tendríamos que utilizar varias etiquetas:

### Saltos de línea ``<br>``

Cuando queremos añadir un ENTER o salto de línea para que el texto baje a la siguiente línea utilizamos la etiqueta ``<br>``. Así, en el caso del ejemplo anterior tendríamos que haber añadido un ``<br>`` para partir la línea del subtítulo:

```
Título: Fenomenología del espíritu

Subtítulo: Contenido de la obra <br>
	La Idea en su ser en y para sí misma, al regresar del gran círculo en que, a partir de su ser
	en sí, recorrió los sucesivos momentos de su alteridad, constituye el objeto de la filosofía
	del espíritu.	

```
Los párrafos se indican con la etiqueta ``<p>``.

Si únicamente añadimos una etiqueta ``<p>`` se aplica un salto de línea algo más grande que el ``<br>`` anterior. Pero si por el contario encerramos un párrafo entre las etiquetas ``<p>`` al principio y ``</p>`` al final del párrafo, éste se separará del bloque anterior y siguiente con un espacio doble (como es el caso de este párrafo).

Así, para separar el título del subtítulo utilizaríamos esta etiqueta:

```
<p>Título: Fenomenología del espíritu</p>

Subtítulo: Contenido de la obra <br>
	La Idea en su ser en y para sí misma, al regresar del gran círculo en que, a partir de su ser
	en sí, recorrió los sucesivos momentos de su alteridad, constituye el objeto de la filosofía
	del espíritu.	

```
### Sangrías  ``<dd>...</dd>``

Las sangrías son aquellos espacios en blanco (vacios) que se colocan al comienzo de una línea o párrafo. Así, para crear sangrías tenemos diferentes etiquetas, aunque posiblemente la que da mejores resultados y es más fácil y fiable son las etiquetas ``<dd>`` y ``</dd>``

```
<p>Título: Fenomenología del espíritu</p>

Subtítulo: Contenido de la obra <br>
	<dd>La Idea en su ser en y para sí misma, al regresar del gran círculo en que, a partir de su ser
	en sí, recorrió los sucesivos momentos de su alteridad, constituye el objeto de la filosofía
	del espíritu.</dd>	

```
### **Negritas** y _cursivas_

     ``<b>...\</b>``   ,   ``<i>...\</i>``

Si queremos colocar **negritas** o _cursivas_ en el texto del ejemplo tenemos que utilizar las etiquetas: ``<b>...</b>`` para negrita y/o ``<i>...<i>`` para cursivas.

Siguiendo con el ejemplo anterior, para colocar "**Título**" y "**Subtítulo**" en **negrita** debemos encerrar estas palabras entre las etiquetas ``<b>`` y ``</b>``.

```
<p><b>Título</b>: Fenomenología del espíritu</p>

<b>Subtítulo</b>: Contenido de la obra <br>
	<dd>La Idea en su ser en y para sí misma, al regresar del gran círculo en que, a partir de su ser
	en sí, recorrió los sucesivos momentos de su alteridad, constituye el objeto de la filosofía
	del espíritu.</dd>

```
Si además, queremos colocar "_Fenomenología del espíritu_" en _cursiva_ debemos encerrar esta palabra entre las etiquetas ``<i>`` e ``</i>``

```
<p><b>Título</b>:<i>Fenomenología del espíritu</i></p>

<b>Subtítulo</b>: Contenido de la obra <br>
	<dd>La Idea en su ser en y para sí misma, al regresar del gran círculo en que, a partir de su ser
	en sí, recorrió los sucesivos momentos de su alteridad, constituye el objeto de la filosofía
	del espíritu.</dd>

```

### Encabezados  ``<h1>``, ``<h2>``, ``<h3>``, ``<h4>``, ``<h5>``, ``<h6>``

Los encabezados (``<h1>``, ``<h2>``, ``<h3>``, ``<h4>``, ``<h5>`` y ``<h6>``) tienen una gran importancia a nivel de SEO, ya que ayudan a posicionar nuestra web. El objetivo es indicar a los buscadores la estructura que tiene cada una de nuestras páginas, de qué va, qué apartados y subapartados tienen y su relación de importancia.

#### ``<h1> ...</h1>`` (Títulos)
Con ``<h1>`` especificamos el título de la página (no del sitio en general) y por lo tanto:

*   Contra más concreto y conciso mejor.
*   Debe definir de qué trata la página.
*   Es importante que sólo exista un único ``<h1>`` por página.
*   Que cada página tengo un ``<h1>`` diferente.
*   Es conveniente colocarlo en la parte superior de la página (antes que los ``<h2>``).

#### ``<h2> ...</h2>`` (Subapartados)

Utilizamos ``<h2>`` para especificar los subtítulos o diferentes partes de cada página. Por ello:

*   Generalmente, su contenido tiene más longitud que los ``<h1>``.
*   Habitualmente existirán varios ``<h2>`` por página.
*   Se colocan al inicio de cada uno de los subapartados.

#### ``<h3> ...</h3>`` (Partes de los subapartados)

La etiqueta ``<h3>`` sirve para especificar las diferentes partes de cada uno de los subapartados.

*   Tiene mucha menos importancia a nivel de SEO.
*   Su uso no es tan generalizada como las anteriores.

Las etiquetas ``<h4>``, ``<h5>`` y ``<h6>`` son etiquetas casi ignoradas para los buscadores, por lo que su uso es muy residual.

Aunque por defecto el navegador muestra cada encabezado con un tamaño predenido según su importancia, es posible modificar este estilo a través de CSS, como veremos en temas posteriores.

El tamaño predefinido para cada uno de los encabezados va de mayor a menor.



## Etiquetas de contenido

Las etiquetas de contenido son las que agrupan el contenido que hay en su interior.


| Elemento | Descripcion |
|----------|-------------|
|`<p>`|Define una parte que debe mostrarse como un párrafo|
|`<hr>`|Representa un cambio temático entre párrafos. Suele representar una línea horizontal|
|`<pre>`|Indica que su contenido está preformateado y que este formato debe ser preservado. (En HTML, cuando no usas `<pre>`, los espacios en blanco múltiples, saltos de línea o tabulaciones se comprimen a un solo espacio)|
|`<blockquote>`|Representa un contenido citado desde otra fuente|
|`<ol>`|Especifica una lista ordenada de elementos|
|`<ul>`|Determina una lista de elementos sin orden|
|`<li>`|Define un elemento de una lista|
|`<dl>`|Especifica una lista de definiciones, es decir, una lista de términos y sus definiciones asociadas|
|`<dt>`|Representa un término definido por el siguiente <dd>|
|`<dd>`|Indica la definición de los términos listados antes que él|
|`<figure>`|Agrupa cualquier contenido que forme parte de un bloque o unidad independiente de información visual o multimedia, que puede ir acompañado de una descripción (<figcaption>). Esto incluye imágenes, videos, audios, y cualquier otro tipo de contenido relacionado|
|`<figcaption>`|Representa la leyenda o título de un elemento `<figure>`|
|`<div>`|Representa un contenedor genérico sin ningún significado especial|

**_Observación1_**: La **diferencia entre usar y no usar la etiqueta `<figure>`** al insertar una imagen radica en su propósito semántico y accesibilidad. Con `<figure>`, se marca el contenido como una unidad independiente relacionada con el texto principal, lo que es útil para imágenes, gráficos o multimedia. **Sin `<figure>`, la imagen simplemente se inserta sin esa estructura semántica ni la opción clara de agregar un pie de foto.**

**_Observación2_**: En **HTML (cuando no usas `<pre>`)**, **los espacios en blanco múltiples, saltos de línea o tabulaciones no se muestran tal cual; se comprimen a un solo espacio** en la mayoría de los casos. Esto significa que, si introduces varios espacios seguidos en el texto, el navegador los tratará como un único espacio. Para incluir múltiples espacios en el flujo normal de texto, es necesario usar entidades HTML como `&nbsp;`. Sin embargo, como veremos más adelante, es preferible usar CSS para controlar el espaciado de manera más flexible y manejable, utilizando propiedades como `margin` o `padding`.

### Código de ejemplo
```
<!-- Elemento <p> -->
<p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Officia beatae aliquam non natus aut id sint ea? Natus tempore hic reprehenderit temporibus minima nisi, quia, magnam omnis, officiis molestiae earum.</p>

<!-- Elemento <hr> -->
<hr>

<!-- Elemento <pre> -->
<pre>Contenido preformateado       Conserva los espacios,
            los saltos de línea y los tabuladores del texto original.
        </pre>

<!-- Elemento <blockquote> -->
<blockquote>Con blockquote representamos un contenido citado desde otra fuente.</blockquote>

<!-- Elemento <ol> -->
<ol>
  <li>Lista ordenada</li>
  <li>Lista ordenada</li>
  <li>Lista ordenada</li>
</ol>

<!-- Elemento <ul> -->
<ul>
  <li>Lista sin orden</li>
  <li>Lista sin orden</li>
  <li>Lista sin orden</li>
</ul>

<!-- Elementos <dl> <dt> <dd>-->
<dl>
  <dt>Término 1</dt>
  <dd>Definición del término 1.</dd>

  <dt>Término 2</dt>
  <dd>Definición del término 2.</dd>

  <dt>Término 3</dt>
  <dd>Definición del término 3.</dd>
</dl>

<!-- Elementos <figure> y <figurecaption>-->
<figure>
  <img src="https://www.eniun.com/wp-content/uploads/eniun-icon-user-experience.svg"
       alt="Usabilidad">
  <figcaption>Figura 1</figcaption>
</figure>

<!-- Elemento <div>-->
<div>Contenedor tipo div</div> 

```


### Atributos más utilizados en etiquetas

Los atributos más usados son _id_ y _class_.

*   _id_: se utiliza para identificar de manera única a un elemento. Como es un **atributo identificativo único**, no debemos añadir dos bloques con el mismo valor de id en el mismo documento HTML.

```
<div id="identificador">Contenedor</div>
```


*   _class_: se utiliza para asignar una o varias clases a un elemento HTML. Las clases son muy útiles para aplicar estilos CSS. **El mismo valor de class se puede asignar a varios elementos**.

```
<div class="clase1 clase2">Contenedor</div>
```

## Etiquetas de texto

Las etiquetas de texto son las que dan significado a los textos que contienen.

| Elemento | Descripción |
|----------|-------------|
|`<a>`|Representa un hiperenlace|
|`<em>`|Especifica un texto enfatizado|
|`<strong>`|Establece un texto importante|
|`<small>`|Define un comentario aparte, es decir, textos de políticas de responsabilidad o una nota de derechos de autoría, que no son esenciales para la comprensión del documento|
|`<s>`|Representa contenido que no es exacto, tiene el estilo tachado|
|`<cite>`|Indica el título de una obra|
|`<q>`|Representa una cita textual entre comillas|
|`<dfn>`|Sirve para marcar el término que se quiere definir|
|`<abbr>`|Envuelve un texto que al pasar el puntero por encima despliega un tooltip. El contenido del tooltip se detalla mediante el atributo title|
|`<time>`|Determina un valor de fecha y hora|
|`<code>`|Establece un código de programación|
|`<sub>``<sup>`|Establece un subíndice y un superíndice respectivamente|
|`<i>`|Muestra el texto marcado con un estilo en cursiva o itálica|
|`<b>`|Representa el texto marcado con un estilo en negrita|
|`<u>`|Muestra el texto subrayado|
|`<mark>`|Representa un texto marcado o resaltado|
|`<span>`|Especifica texto en línea. Sirve para aplicar estilo al texto o agrupar elementos en línea|
|`<br>`|Inserta un salto de línea|
|`<wbr>`|Indica una oportunidad de salto de línea, es decir, un punto sugerido donde el texto puede ser dividido para mejorar su legibilidad|


### Código de ejemplo
```
<!-- Elemento <a>-->
<a href="https://www.eniun.com">Esto es un hiperenlace</a>

<!-- Elemento <em>-->
<em>Esto es un texto enfatizado.</em>

<!-- Elemento <strong>-->
<strong>Esto es un texto importante.</strong>

<!-- Elemento <small>-->
<small>Nota de derechos</small>

<!-- Elemento <s>-->
<s>Este texto no es exacto</s>

<!-- Elemento <cite>-->
<cite>Este es el título de una obra</cite>

<!-- Elemento <q>-->
<q>Representa una cita textual entre comillas.</q>

<!-- Elemento <dfn>-->
<p>El <dfn>HTML</dfn> es un lenguaje de marcado.</p>

<!-- Elemento <abbr>-->
<p>Pasa el puntero por encima de la siguiente etiqueta abbr: <abbr title="Hypertext Markup Language">HTML</abbr></p>

<!-- Elemento <time>-->
<time>15s</time>

<!-- Elemento <code>-->
<code>h1{color:red;}</code>  

<!-- Elemento <var>-->
<p>El bucle no se detiene hasta que <var>centinela</var> sea igual a 0.</p> 

<!-- Elemento <samp>-->
<p>Al presionar e botón aparecerá una ventana con el mensaje: <samp>Bienvenido</samp>
</p>

<!-- Elemento <kbd>-->
<p> Si está conforme escriba presione <kbd>sí</kbd>. Si no, pulse <kbd>no</kbd>.
</p>

<!-- Elementos <sub> <sup>-->
<p>La fórmula química de agua es H<sub>2</sub>O</p>
<p>Trade Mark <sup>TM</sup></p>

<!-- Elemento <i>-->
<i>Texto en italica</i>

<!-- Elemento <b>-->
<b>Texto en negrita</b>

<!-- Elemento <u>-->
<u>Texto subrayado</u>

<!-- Elemento <mark>-->
<p>El siguiente texto tiene mucha importancia y quiero resaltarlo: <mark>HTML5</mark></p>

<!-- Elemento <span>-->
<span>Texto </span><span>en </span><span>línea.</span>

<!-- Elemento <br>-->
<br>

<!-- Elemento <wbr>-->       <p>https://www.eniun.com<wbr>/deeper<wbr>/level<wbr>/pages<wbr>/deeper<wbr>/level<wbr>/pages<wbr>/deeper<wbr>/level<wbr>/pages<wbr>/deeper<wbr>/level<wbr>/pages<wbr>/deeper<wbr>/level<wbr>/pages</p>

```

### Caracteres especiales

Dentro de una página web no podemos poner directamente los caracteres «<» Y «>» porque el navegador los confundiría con los caracteres que se utilizan para la creación de etiquetas HTML.

Para cierto tipo de caracteres, es necesario utilizar otra sintaxis o codificación de caracteres. A continuación veremos la representación ASCII de los símbolos mediante entidades, código decimal y hexadecimal.

1.  **Entidades HTML**: Las entidades HTML son secuencias de caracteres que representan símbolos especiales en HTML. Comienzan con un ampersand (&), seguido de un nombre o número y terminan con un punto y coma (;). Las entidades HTML son fáciles de leer y entender, lo que las hace convenientes para usar en el código HTML.
2.  **Códigos decimales:** Los códigos decimales son valores numéricos que representan símbolos en la tabla ASCII. Estos códigos se escriben en la forma «&#n;», donde «n» es el número decimal correspondiente al símbolo. Los códigos decimales son útiles cuando no se puede utilizar una entidad HTML específica o cuando se necesita una representación numérica precisa del símbolo.
3.  **Códigos hexadecimales**: Los códigos hexadecimales son valores numéricos en base 16 que representan símbolos en la tabla ASCII. Los códigos hexadecimales son similares a los códigos decimales, pero utilizan una representación en base 16 en lugar de base 10. Estos códigos se escriben en la forma «&#xn;», donde «n» es el valor hexadecimal correspondiente al símbolo.

En la siguiente tabla se muestran algunos símbolos y su correspondiente código decimal y su entidad HTML:


|Símbolo|Código decimal|Entidad |
|-------|--------------|--------|
|&      |&#38;         |&amp;   |
|<      |&#60;         |&lt;    |
|“      |&#34;         |&quot;  |
|>      |&#62;         |&gt;    |
|©      |&#169;        |&copy;  |
|÷      |&#247;        |&divide;|
|€      |&#8364;       |&euro;  |
|←      |&#8592        |&larr;  |


Aquí puedes ver una tabla ASCII estándar con los códigos y los nombres de las entidades en HTML: [ascii.cl/es/codigos-html.htm](https://ascii.cl/es/codigos-html.htm). En el siguiente enlace puedes ver más símbolos especiales [webusable.com/CharsExtendedTable.htm](http://www.webusable.com/CharsExtendedTable.htm)

