
Etiquetas básicas
-----------------

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

Saltos de línea \<br>
-----------------------

Cuando queremos añadir un ENTER o salto de línea para que el texto baje a la siguiente línea utilizamos la etiqueta \<br>. Así, en el caso del ejemplo anterior tendríamos que haber añadido un \<br> para partir la línea del subtítulo:

```
Título: Fenomenología del espíritu

Subtítulo: Contenido de la obra <br>
	La Idea en su ser en y para sí misma, al regresar del gran círculo en que, a partir de su ser
	en sí, recorrió los sucesivos momentos de su alteridad, constituye el objeto de la filosofía
	del espíritu.	

```


Los párrafos se indican con la etiqueta \<p>.

Si únicamente añadimos una etiqueta \<p> se aplica un salto de línea algo más grande que el \<br> anterior. Pero si por el contario encerramos un párrafo entre las etiquetas \<p> al principio y </p> al final del párrafo, éste se separará del bloque anterior y siguiente con un espacio doble (como es el caso de este párrafo).

Así, para separar el título del subtítulo utilizaríamos esta etiqueta:

```
<p>Título: Fenomenología del espíritu</p>

Subtítulo: Contenido de la obra <br>
	La Idea en su ser en y para sí misma, al regresar del gran círculo en que, a partir de su ser
	en sí, recorrió los sucesivos momentos de su alteridad, constituye el objeto de la filosofía
	del espíritu.	

```


Sangrías    \<dd>...\</dd>
------------------------

Las sangrías son aquellos espacios en blanco (vacios) que se colocan al comienzo de una línea o párrafo. Así, para crear sangrías tenemos diferentes etiquetas, aunque posiblemente la que da mejores resultados y es más fácil y fiable son las etiquetas \<dd> y \</dd>

```
<p>Título: Fenomenología del espíritu</p>

Subtítulo: Contenido de la obra <br>
	<dd>La Idea en su ser en y para sí misma, al regresar del gran círculo en que, a partir de su ser
	en sí, recorrió los sucesivos momentos de su alteridad, constituye el objeto de la filosofía
	del espíritu.</dd>	

```


**Negritas** y _cursivas_
-------------------------

     \<b>...\</b>   ,   \<i>...\</i>

Si queremos colocar **negritas** o _cursivas_ en el texto del ejemplo tenemos que utilizar las etiquetas: \<b>...\</b> para negrita y/o \<i>...\<i> para cursivas.

Siguiendo con el ejemplo anterior, para colocar "**Título**" y "**Subtítulo**" en **negrita** debemos encerrar estas palabras entre las etiquetas \<b> y \</b>.

```
<p><b>Título</b>: Fenomenología del espíritu</p>

<b>Subtítulo</b>: Contenido de la obra <br>
	<dd>La Idea en su ser en y para sí misma, al regresar del gran círculo en que, a partir de su ser
	en sí, recorrió los sucesivos momentos de su alteridad, constituye el objeto de la filosofía
	del espíritu.</dd>

```


Si además, queremos colocar "_Fenomenología del espíritu_" en _cursiva_ debemos encerrar esta palabra entre las etiquetas \<i> e \</i>

```
<p><b>Título</b>:<i>Fenomenología del espíritu</i></p>

<b>Subtítulo</b>: Contenido de la obra <br>
	<dd>La Idea en su ser en y para sí misma, al regresar del gran círculo en que, a partir de su ser
	en sí, recorrió los sucesivos momentos de su alteridad, constituye el objeto de la filosofía
	del espíritu.</dd>

```


Encabezados    \<h1>, \<h2>, \<h3>, \<h4>, \<h5>, \<h6>
--------------------------------------------------------

Los encabezados (\<h1>, \<h2>, \<h3>, \<h4>, \<h5> y \<h6>) tienen una gran importancia a nivel de SEO, ya que ayudan a posicionar nuestra web. El objetivo es indicar a los buscadores la estructura que tiene cada una de nuestras páginas, de qué va, qué apartados y subapartados tienen y su relación de importancia.

### \<h1> ...\</h1>  
Con \<h1> especificamos el título de la página (no del sitio en general) y por lo tanto:

*   Contra más concreto y conciso mejor.
*   Debe definir de qué trata la página.
*   Es importante que sólo exista un único \<h1> por página.
*   Que cada página tengo un \<h1> diferente.
*   Es conveniente colocarlo en la parte superior de la página (antes que los <h2> ).

### \<h2> ...\</h2>   (subapartados)

Utilizamos \<h2> para especificar los subtítulos o diferentes partes de cada página. Por ello:

*   Generalmente, su contenido tiene más longitud que los \<h1>.
*   Habitualmente existirán varios \<h2> por página.
*   Se colocan al inicio de cada uno de los subapartados.

### \<h3> ...\</h3>   (partes de los subapartados)

La etiqueta \<h3> sirve para especificar las diferentes partes de cada uno de los subapartados.

*   Tiene mucha menos importancia a nivel de SEO.
*   Su uso no es tan generalizada como las anteriores.

Las etiquetas \<h4>, \<h5> y \<h6> son etiquetas casi ignoradas para los buscadores, por lo que su uso es muy residual.

Aunque por defecto el navegador muestra cada encabezado con un tamaño predenido según su importancia, es posible modificar este estilo a través de CSS, como veremos en temas posteriores ([estilos CSS para textos](https://www.html6.es/t3_2_propiedades.html#punto2)).

El tamaño predefinido para cada uno de los encabezados va de mayor a menor.