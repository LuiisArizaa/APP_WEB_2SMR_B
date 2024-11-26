# Qué son las abreviaciones Emmet con ejemplos prácticos
Las **abreviaciones Emmet** son una herramienta que nos permite **escribir código HTML y CSS de manera más rápida**. A través de abreviaciones, Emmet expande fragmentos de código en estructuras completas, lo que reduce el tiempo necesario para crear etiquetas y elementos repetitivos. Su uso agiliza el flujo de trabajo, permitiendo concentrarse más en la lógica y diseño que en la sintaxis básica.

## Cómo usar abreviaciones Emmet en VSCode

A continuación, se presentan algunos ejemplos de cómo utilizar estas abreviaciones para optimizar tu código. Puedes encontrar más información en la **[documentación oficial](https://docs.emmet.io/cheat-sheet/)**

Veamos qué son las abreviaciones EMMET con varios ejemplos que puedes ir probando en tu código para generar rápidamente etiquetas HTML:

### 1\. Crear una estructura básica de HTML

**Abreviación**: `!`  
**Resultado**:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>

</body>
</html>
```


### 2\. Crear un div con una clase

**Abreviación**: `.container`  
**Resultado**:

```
<div class="container"></div>
```


### 3\. Crear un div con múltiples clases

**Abreviación**: `div.class1.class2`  
****Resultado****:

```
<div class="class1 class2"></div>
```


### 4\. Crear un elemento con un id y clase

**Abreviación**: `div#header.container`  
****Resultado****:

```
<div id="header" class="container"></div>
```


### 5\. Crear una lista desordenada con elementos de lista

**Abreviación**: `ul>li*5`  
****Resultado****:

```
<ul>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
    <li></li>
</ul>
```


### 6\. Crear una lista con contenido en cada elemento

**Abreviación**: `ul>li.item$*5`  
****Resultado****:

```
<ul>
    <li class="item1"></li>
    <li class="item2"></li>
    <li class="item3"></li>
    <li class="item4"></li>
    <li class="item5"></li>
</ul>
```


### 7\. Crear un enlace con texto

**Abreviación**: `a[href="https://google.com"]{Google}`  
****Resultado****:

```
<a href="https://google.com">Google</a>
```


### 8\. Crear un formulario con varios campos

**Abreviación**: `form>input[type="text"]+input[type="email"]+input[type="submit"]`  
****Resultado****:

```
<form>
    <input type="text">
    <input type="email">
    <input type="submit">
</form>
```


### 9\. Crear una tabla con filas y columnas

**Abreviación**: `table>tr*3>td*3`  
****Resultado****:

```
<table>
    <tr>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
    </tr>
</table>
```


### 10\. Crear una sección con encabezado y párrafo

**Abreviación**: `section>h2+p`  
****Resultado****:

```
<section>
    <h2></h2>
    <p></p>
</section>
```


### 11\. Crear un grupo de imágenes con atributos

**Abreviación**: `img[src="image$"].image*3`  
****Resultado****:

```
<img src="image1" class="image">
<img src="image2" class="image">
<img src="image3" class="image">
```


### 12\. Crear un párrafo con texto:

**Abreviación**: `p{Este es un párrafo}`  
**Resultado**:

```
<p>Este es un párrafo</p>
```


### 13\. Crear un botón con texto

**Abreviación**: `button{Enviar}`  
**Resultado**:

```
<button>Enviar</button>
```


### 14\. Crear una etiqueta de imagen con `alt` y `src`

**Abreviación**: `img[src="image.jpg" alt="Descripción de la imagen"]`  
**Resultado**:

```
<img src="image.jpg" alt="Descripción de la imagen">
```


### 15\. Crear una estructura de encabezado (`header`) con un título y un enlace

**Abreviación**: `header>h1{Bienvenido}+a[href="#"]{Inicio}`  
**Resultado**:

```
<header>
    <h1>Bienvenido</h1>
    <a href="#">Inicio</a>
</header>
```


### 16\. Crear una etiqueta de `input` de tipo texto con un `placeholder`

**Abreviación**: `input[type="text" placeholder="Escribe aquí"]`  
**Resultado**:

```
<input type="text" placeholder="Escribe aquí">
```


Estos son solo algunos ejemplos de uso de algunas abreviaciones Emmet. Puedes explorar la [**documentación oficial**](https://docs.emmet.io/) para descubrir más abreviaciones.