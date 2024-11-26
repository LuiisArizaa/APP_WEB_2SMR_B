# Enlaces

## Enlaces (de texto)

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

###  Enlazar con páginas HTML propias hechas por nosotros

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

## Valores del atributo href

Como hemos visto, el elemento <a> o hiperenlace crea un enlace a otra página o archivo. Además, también puede enlazar a una sección de la misma página, a un correo electrónico o a un teléfono, entre otras opciones.

**Valores del atributo href:** vamos a ver cómo crear un enlace para llamar a un número de teléfono con **tel** y para enviar un correo con **mailto**.


### Ejemplo
```
<!-- Enviar un correo con mailto-->
<a href="mailto:info@eniun.com">Enviar correo a Eniun</a><br>
<!-- Llamar por teléfono con tel-->
<a href="tel:+34666666666">Llamar por teléfono a 666 666 666</a>

```

## Valores del atributo target

El atributo «target» en HTML se utiliza para especificar dónde se debe abrir el enlace cuando un usuario hace clic en él. A continuación se presentan algunos de los valores más comunes utilizados para el atributo «target»:

|Valor|Descripción|
|-----|-----------|
|«_blank»|Abre el enlace en una nueva ventana o pestaña del navegador|
|«_self»|Abre el enlace en la misma ventana o pestaña del navegador (valor predeterminado)|
|«_parent»|Abre el enlace en el marco principal o padre en caso de que se esté utilizando frames|
|«_top»|Abre el enlace en la ventana principal del navegador, reemplazando cualquier frame existente|

### Ejemplo

En el siguiente ejemplo vamos a abrir un enlace en una página distinta mediante el atributo target y el valor \_blank.

```
<!-- Abrir enlace en una página aparte -->
<a href="https://www.eniun.com" target="_blank">Enlace 1</a>
 
<!-- Abrir enlace en la misma página -->
<a href="https://www.eniun.com" target="_self">Enlace 2</a>

```


### Atributo download

El atributo «**download**» en HTML se utiliza para especificar que un enlace debe ser descargado al hacer clic en él en lugar de navegar hacia él. Permite proporcionar un nombre de archivo sugerido para el archivo descargado. Así es como funciona el atributo «download»:

```
<a href="ruta/al/archivo.pdf" download="miarchivo.pdf">Descargar PDF</a>
```

En este ejemplo, cuando el usuario hace clic en el enlace «Descargar PDF», en lugar de abrirse en el navegador, se descargará el archivo especificado en el atributo «href» (`ruta/al/archivo.pdf`). El atributo «download» especifica el nombre de archivo sugerido para el archivo descargado (`miarchivo.pdf`).










