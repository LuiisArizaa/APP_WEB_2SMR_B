# Enlaces
Enlaces (de texto)
------------------

Podemos encontrar 6 tipos de enlaces:

1.  A páginas [HTML externas propias](#punt1) hechas por nosotros.
2.  A [partes internas](#punt2) del mismo HTML.
3.  A páginas [HTML de terceros](#punt3).
4.  A un [correo electrónico](#punt4).
5.  A [ficheros](#punt5) pdf, jpg, gif, png, svg.
6.  A [ficheros comprimidos](#punt6) para ser descargados (zip).

En todos los casos utilizamos la misma etiqueta \<a> para abrir y \</a> para cerrar:

```
<a href="fichero_a_abrir.html"> Enlace </a>

```
* **href** sería el atributo donde se tiene que indicar el lugar donde accederá el usuario cuando haga clic en dicho enlace.  
fichero\_a\_abrir.html indica el fichero, dirección de correo electrónico o parte del mismo documento donde se desea acceder.  

* **Enlace** sería el texto (o la imagen) sobre la que el usuario tendría que hacer clic para acceder al destino indicado.

### Enlazar con páginas HTML propias hechas por nosotros

Como normalmente ubicaremos los distintos ficheros HTML en la misma carpeta, para enlazar un HTML con otro, únicamente hay que especificar el archivo HTML al que se desea enlazar (sin olvidar de indicar el formato .html).

En el siguiente ejemplo se crea un enlace de texto, que será "Galería de Imágenes", y que -al hacer clic- comunicará con el archivo galeria.html (ubicados ambos ficheros en la misma carpeta):

```
<a href="galeria.html">Galería de Imágenes</a>

```


### Enlaces a una parte interna de nuestro HTML

Es posible realizar un enlace que comunique con **una parte en concreto** de nuestro HTML (ya sea del mismo documento o bien de otro), como por ejemplo los típicos enlaces que te llevan al principio de la página.

Para ello hay que especificar a qué parte del documento HTML se desea acceder, especificando el nombre id de un elemento ubicado en dicho lugar, anteponiendo el símbolo '#' antes de dicho nombre. Es decir, es necesario que exista una etiqueta HTML con el nombre id especificado (id="nombre"), y que además esté ubicado en el lugar del HTML al que se desea acceder.

Por ejemplo, si queremos crear un enlace que comunique con el inicio del mismo documento y en dicho lugar existe un \<div> que tiene un id llamado inicio, utilizaríamos el siguiente código:

Enlace dentro del mismo documento:

```
<a href="#inicio">Enlace</a>

```


Enlace al mismo punto, pero desde fuera del mismo documento (desde otro documento html distino):

```
<a href="galeria.html#inicio">Enlace</a>

```


### Enlazar con páginas HTML de terceros:

Para enlazar con páginas web externas realizadas por otras personas, tendremos que añadir el atributo target="\_blank", para que dicha página no se abra en la misma ventana del navegador (cerrando por lo tanto nuestra web) y que ésta se abra en una nueva pestaña del navegador.

Otro de los puntos importantes es que la dirección de la web de destino tiene que empezar obligatoriamente por http o https.

```
<a href="https://www.html6.es/t1_estructura.html" target="_blank">Galería de Imágenes</a>

```


### Enlazar con un correo electrónico

Aunque el mejor método para poder enviar un correo electrónico es a través de un formulario y utilizando un pequeño código de PHP, para salir del paso podemos utilizar el prefijo mailto:, seguido de la dirección de correo electrónico.

```
<a href="mailto:jab@jabmultimedia.com">Enviar mail</a>

```


El gran problema de este código es que al hacer clic sobre dicho enlace, se abrirá el programa predeterminado de correo electrónico que esté instalado en el ordenador utilizado, con el correo electrónico de destino ya escrito para que el usuario envie el mail desde este programa de correo. Esto quiere decir que si no existe ningún programa de correo configurado (como es el caso de un cibercafé, biblioteca o del aula de informática de cualquier centro educativo) no será posible enviar ningún mail.

### Enlazar con ficheros pdf, jpg, gif, png, svg...

El navegador puede abrir un gran número de extensión de ficheros. Así, si enlazamos con un fichero pdf, una imagen o algunos formatos de archivo determinados, el navegador los podrá mostrar sin ningún problema. Si no lo puede abrir se descargarán en la carpeta de 'Descargas'.

Si dicho archivo está en la misma carpeta que el archivo HTML, se especificará únicamente el nombre del archivo y su extensión sin más, mientras que si está en Internet habrá que especificar la ruta entera (empezando con http o https).

```
<a href="carpeta/informe.pdf" target="_blank">Ver informe</a>

```


### Enlazar con ficheros comprimidos para descargar

Para permitir que los usuarios se puedan descargar los ficheros que creamos convenientes, es suficiente con comprimir todos los ficheros en un archivo comprimido (zip o rar), colgarlo en nuestro servidor y enlazar directamente con dicho fichero.

```
<a href="carpeta/trabajos.zip">Descargar los trabajos</a>

```


Con este cógido el navegador descargará el archivo especificado y lo guardará en la carpeta de descargas.

Imágenes como enlace
--------------------

Para que el enlace sea una imagen (y no un texto) es suficiente con sustituir el texto del enlace por la etiqueta \<img> (utilizada para mostrar imágenes y explicada en el tema [Imágenes](https://www.html6.es/t1_4_imagenes.html)).

```
<a href="galeria.html">
    <img src="carpeta/imagen.png">
</a>

```


CSS exclusivo para enlaces
--------------------------

Si -por ejemplo- queremos tener el siguiente enlace de color **naranja**:

```
<nav id="enlaces">
   <a href="galeria.html">Ir a Galería</a>
</nav>

```


El siguiente código CSS sería totalmente **erróneo**:

```
#enlaces{
   color:orange;
}

```


Ya que el selector #enlaces cambiaría a color naranja todos los **textos** que hubiesen dentro de la caja \<nav> llamada "enlaces", pero como el enlace "Ir a Galería" no es un texto, sino que es un enlace, lo que tenemos que utilizar es el selector a, en vez de indicar el nombre de su caja:

```
#enlaces a{
   color:orange;
}

```


O, si queremos que este color se aplique a **todos los enlaces** de la página podemos generalizar, sin indicar la caja donde se encuentra el enlace:

Si además queremos que el enlace NO esté subrayado utilizaremos la propiedad text-decoration, con un valor none, que también se tiene que aplicar al enlace (a) y no a la caja donde esté el enlace:

```
a{
   text-decoration:none;
   color:orange;
}

```


Para que al pasar por encima del enlace éste se coloree de color rojo, utilizaremos la pseudo-clase (o evento) **:hover**;

Por último, si queremos que:

1.  Un enlace no funcione como enlace en un HTML en concreto (ya que ya estamos en esa misma página) y por lo tanto al pulsar sobre el enlace se recargaría la misma página en la que ya estamos.
2.  Que dicho enlace en concreto tenga un aspecto diferente al resto de enlaces para informar al usuario del apartado en el que encuentra en este momento.
3.  Que cuando el usuario pase con el cursor por encima, el aspecto del cursor no cambie y continue siendo el de la flecha blanca.

Tendremos que utilizar dos selectores CSS, uno para el aspecto de inicio y el otro para indicar las características para cuando el cursor pase por encima.

```
<nav>
    <div id="enlace1" class="enlaces">
       <a>Ir a Galería</a>
    </div>
</nav>

```


Eliminando el atributo href de la etiqueta \<a>, el enlace no funciona como enlace (no enlaza con nada al hacer clic), pero sigue cambiando de color al colocar el cursor encima. El problema es que el cursor que aparece al colocar el mouse encima es muy poco apropiado (el de selección de texto: (coloca el cursor encima del siguiente enlace para ver el cursor de 'selección de texto'): Ir a Galería).

Así, para especificar el color de inicio del enlace utilizamos el selector **#enlace1 a**, mientras que dentro de **#enlace1 a:hover** especificamos el cursor (el habitual) que aparecerá al colocar el mouse encima.

```
#enlace1 a{
    color:chocolate;
    font-size:20px;	
}

#enlace1 a:hover{
    cursor:default;
}

```
