# Listas
Listas
------

Las listas son muy útiles cuando queremos ofrecer una lista de elementos, palabras, frases o enlaces uno debajo del otro. Si estos elementos van encabezados por una bolita o un cuadrado son listas no ordenadas, si por el contrario van encabezados por números (correlativos: 1, 2...), letras ordenadas alfabeticamente (A, B...) o números romanos (I, II...) son listas ordenadas.

Así, para crear listas utilizamos dos etiquetas.

*   \<ul> y \</ul> para listas no ordenadas (señaladas por bolitas o cuadrados).
*   \<ol> y \</ol> para listas ordenadas (señaladas por números o letras).

En ambos casos, cada uno de los términos o elementos (ordenados o no) que van a componer la lista se deben encerrar entre las etiquetas \<li> y \</li>.

Para mostrar algunos ejemplos vamos a utilizar la muy útil, interesante, actual, cónica y boreal lista de los **Reyes Godos** recortada en versión remix.

### Ejemplo de lista no ordenada

```
Esto es una lista no ordenada de los primeros Reyes Godos (del conocidísimo Reino Tolosano):  
<ul>
    <li> Ataúlfo (410-415) </li>    
    <li> Sigérico (415) </li>    
    <li> Walia (415-418) </li>    
    <li> Teodorico I (418-451) </li>
</ul>

```


El resultado en el navegador es:

Esto es una lista **no ordenada** de los primeros Reyes Godos (del conocidísimo Reino Tolosano):

*   Ataúlfo (410-415)
*   Sigérico (415)
*   Walia (415-418)
*   Teodorico I (418-451)

### Ejemplo de lista ordenada

```
Esto es una lista ordenada de los primeros Reyes Godos (del Reino Visigodo-Católico): 		
<ol>    
    <li> Recaredo (586-601) </li>
    <li> Liuva II (601-603) </li>
    <li> Witérico (603-610) </li>
    <li> Gundemaro (610-612) </li>
</ol>

```


El resultado en el navegador es:

Esto es una lista **ordenada** de los primeros Reyes Godos (del Reino Visigodo-Católico):

1.  Recaredo (586-601)
2.  Liuva II (601-603)
3.  Witérico (603-610)
4.  Gundemaro (610-612)

Listas no ordenadas
-------------------

De manera predefinida delante de cada línea de la lista se coloca automáticamente como viñeta un pequeño círculo negro (llamado **disc**). Si queremos otro tipo de viñeta podemos especificarlo en la etiqueta \<ul> añadiendo el atributo type, seguido de los valores circle para utilizar círculos sin relleno o square para cuadrados.

```
<ul type="circle"> (visualiza círculos sin relleno como viñetas).
```


Lista (**no ordenada**) con viñetas de tipo circle de los primeros Reyes Godos (del Reino Arriano):

*   Gesaleico (507-510)
*   Amalarico, bajo la regencia de Teodorico (510-526)
*   Theudis (534-548)

  

```
<ul type="square"> (visualiza cuadrados como viñetas).
```


Lista (**no ordenada**) con viñetas de cuadrados de tipo (square) de los últimos Reyes Godos (de todos los reinos):

*   Egica y Witiza (698/700-702)
*   Witiza, rey único (702-710)
*   Rodrigo (710-711)

Listas ordenadas
----------------

Por defecto, para numerar las listas ordenadas se utilizan números (que empiezan por el 1). Para utilizar letras mayúsculas, minúsculas o números romanos podemos añadir el atributo type, seguido de uno de los siguientes valores:

*   A: para letras mayúsculas.
*   a: para letras minúsculas.
*   I: para números romanos en mayúscula.
*   i: para números romanos en minúscula.

Por ejemplo, utilizando el código:

```
<ol type="A"> (se crea una lista ordenada alfabeticamente por letras mayúsculas).
```


Lista (**ordenada**) con letras mayúsculas de los Reyes Godos con los nombres más _in_ del momento:

1.  Sisebuto (612-621)
2.  Atanagildo (555-567)
3.  Leovigildo (571/72-586)

Además, podemos indicar por qué número o letra tiene que empezar a "contar", añadiendo el atributo start:

```
<ol start="4"> (empezará la lista por el número 4 y utilizará números ya que no hemos especificado ningún valor en type).
```


Lista (ordenada) que se inicia en el número 4 de los Reyes Godos con los nombres más _in_ del momento (bis):

4.  Ervigio (680-687)
5.  Sisenando (631-636)
6.  Gundemaro (610-612)

Por último, también es posible utilizar de manera conjunta los atributos type y start:

```
<ol type="a"" start="2"> (crea una lista ordenada alfabeticamente por letras minúsculas que empiezan por la segunda letra).
```

Lista (ordenada) que se inicia en la segunda letra minúscula de los últimos Reyes Godos del Reino Tolosano:

2.  Turismundo (451-453)
3.  Theudiselo (548-549)
4.  Teodorico II (453-466)

Listas con imágenes en vez de viñetas
-------------------------------------

Tenemos la posibilidad de sustituir las viñetas predeterminadas (círculos o cuadros) por imágenes (gif o png) añadiendo un poco de código CSS.

Vamos a añadir un icono de una flecha en formato PNG (![](https://www.html6.es/img_html/flecha_derecha.png)) -que tenemos en la carpeta img\- delante de cada elemento de la siguiente lista:

```
<ul class="lista1">
   <li> Ataúlfo (410-415) </li>
   <li> Sigérico (415) </li>
   <li> Walia (415-418) </li>
   <li> Teodorico I (418-451) </li>
</ul>

```


Código CSS:

```
.lista1{
   list-style:none; 
   list-style-image:url('img/flecha.gif');
}

```


Así, con **list-style: none;** eliminamos las viñetas, mientras que con list-style-image especificamos qué imagen se debe utilizar.

![](https://www.html6.es/img_html/flecha_derecha.png) Ataúlfo (410-415)

![](https://www.html6.es/img_html/flecha_derecha.png) Sigérico (415)

![](https://www.html6.es/img_html/flecha_derecha.png) Walia (415-418)

![](https://www.html6.es/img_html/flecha_derecha.png) Teodorico I (418-451)

Viñetas de colores
------------------

Mis Reyes Godos preferidos:

*   Ataúlfo (410-415)
*   Sigérico (415)
*   Walia (415-418)
*   Teodorico I (418-451)

Normalmente el texto y la viñeta (círculo o cuadrado) de cada elemento de la lista comparten el mismo color, tipo y tamaño de la fuente, por lo que si queremos independizar a estos dos elementos para darles a cada uno de ellos por separado un estilo diferente, vamos a tener que encerrar al texto dentro de una etiqueta \<span>, para que de esta manera podamos hacer referencia a este tipo de etiqueta en el código CSS sin influir en las características de la viñeta.

Vamos a hacer un ejemplo con una versión resumida de una lista de mis Reyes Godos preferidos.

```
<ul>
   <li> <span>Ataúlfo (410-415)</span> </li>
   <li> <span>Sigérico (415)</span> </li>
   <li> <span>Walia (415-418)</span> </li>
   <li> <span>Teodorico I (418-451)</span> </li>
</ul>

```


```
<style type="text/css">
    ul li{
       color:red;
       font-weight:bold;
       font-size:8px;
    }
    ul li span{
       color:black;
       font-size:15px;
    }   
</style>

```


Con 'ul li' estamos haciendo referencia a cada uno de los elementos \<li> de la lista \<ul>, osea a las viñetas (bolitas o cuadrados).

Con 'ul li span' agrupamos a todas las etiquetas de tipo \<span>, que se encuentren dentro de las etiquetas de tipo \<li> y que a su vez éstas estén dentro de etiquetas \<ul>. En este caso se refiere a los textos de las viñetas, a los que se les aplica un color negro y un tamaño de 15 píxeles.