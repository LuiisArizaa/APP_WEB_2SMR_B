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

## Atributos de las listas en HTML

Los atributos de las listas en HTML te permiten personalizar tanto las listas ordenadas como las listas no ordenadas. A continuación se muestra una descripción de algunos de los atributos más comunes para ambos tipos de listas:

Los **atributos type y start** **no son soportados en algunas versiones de HTML** (por ejemplo en HTML 4.01 strict). En cualquier caso, lo **recomendable es hacer uso de hojas de estilo CSS**, usando propiedades como `list-style-type` u otras, como veremos en la unidad de CSS.

Atributo «**type**» (para listas ordenadas):

*   «1»: Numeración decimal (1, 2, 3, …).
*   «A»: Letras mayúsculas (A, B, C, …).
*   «a»: Letras minúsculas (a, b, c, …).
*   «I»: Números romanos mayúsculos (I, II, III, …).
*   «i»: Números romanos minúsculos (i, ii, iii, …).

Atributo «**type**» (para listas no ordenadas):

*   «disc»: Puntos sólidos (●, ●, ●, …).
*   «circle»: Círculos (○, ○, ○, …).
*   «square»: Cuadrados (■, ■, ■, …).

Atributo «**start**» (solo para listas ordenadas): Establece el valor inicial de la numeración de la lista.

Atributo «**reversed**» (solo para listas ordenadas): Invierte el orden de numeración de la lista.

A continuación se muestra un ejemplo del uso de estos atributos:

```
<h3>Lista ordenada 1:</h3>
<ol type="A" start="3">
  <li>Elemento 1</li>
  <li>Elemento 2</li>
  <li>Elemento 3</li>
</ol>

<h3>Lista ordenada 2:</h3>
<ol type="1" reversed>
  <li>Elemento 1</li>
  <li>Elemento 2</li>
  <li>Elemento 3</li>
</ol>

<h3>Lista no ordenada 3:</h3>
<ul type="square">
  <li>Elemento 1</li>
  <li>Elemento 2</li>
  <li>Elemento 3</li>
</ul>
```


En este ejemplo, la lista ordenada 1 comenzará en la letra «C» y la lista ordenada 2 invertirá el orden numérico de los elementos. La lista no ordenada utilizará cuadrados como viñetas. Ver ejemplo en CodePen:


