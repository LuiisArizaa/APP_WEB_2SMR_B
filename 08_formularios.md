# Etiquetas para la creación de formularios

Los formularios son los elementos en los que se integran los botones y las áreas de texto que se utilizan para que los usuarios introduzcan sus datos o que puedan elegir entre varias opciones. Veamos las etiquetas que se utilizan para la **creación de formularios en HTML5**.

--- 

El principio y final de un formulario se define con las etiquetas `<form>` y `</form>`. Dentro de las etiquetas de apertura y cierre de form se pueden incluir diferentes elementos que son enviados para ser procesados por el servidor web. Ejemplo:

```
<form action="procesar-registro.php" method="POST">
  <label for="name">Name:</label>
  <input type="text" id="name" required>

  <label for="email">Email:</label>
  <input type="email" id="email" required>

  <input type="submit" value="Submit">
</form>
```


4.1. Atributos de la etiqueta `form`
------------------------------------

El atributo _action_ en un elemento `<form>` especifica la URL o ruta a la cual se enviarán los datos del formulario cuando este sea enviado. Por otro lado, el atributo _method_ define el método HTTP que se utilizará para enviar los datos del formulario.

*   _action_: Puede ser una URL relativa o absoluta que indica dónde se enviarán los datos del formulario para su procesamiento. Por lo general, se especifica la URL de un script del lado del servidor que se encargará de procesar los datos del formulario. Por ejemplo:

```
<form action="/procesar-formulario" method="POST">
  <!-- Campos del formulario -->
</form>
```


En este caso, los datos del formulario se enviarán a la ruta «/procesar-formulario» en el servidor.

El atributo _method_ puede ser «_GET_» o «_POST_» y determina el método HTTP que se utilizará para enviar los datos del formulario al servidor. La diferencia principal radica en cómo se transmiten los datos.

*   _**GET**_: Los datos del formulario se adjuntan a la URL como parámetros de consulta. Es la forma predeterminada si no se especifica el atributo method. Es útil cuando se desea que los datos del formulario sean visibles en la URL, por ejemplo, al realizar búsquedas.

*   _**POST**_: Los datos del formulario se envían en el cuerpo de la solicitud HTTP de manera más segura y no se muestran en la URL. Es adecuado para enviar datos sensibles, como contraseñas o información personal.

4.2. Etiquetas para la creación de formularios
----------------------------------------------

HTML5 dispone de un gran número de elementos de formulario como puedes ver en la siguiente tabla.


|Elemento| Descripcion|
|--------|------------|
|`<form>`|Define un formulario|
|`<fieldset>`|Permite organizar en grupos los campos de un formulario|
|`<legend>`|Representa el título de un `<fieldset>`|
|`<label>`|Representa el título de un elemento de control de un formulario|
|`<input>`|Se usa para crear controles interactivos que reciben datos del usuario|
|`<button>`|Representa un botón|
|`<select>`|Representa un elemento de control que permite la selección entre un conjunto de opciones `<option>`|
|`<option>`|Representa una opción en un elemento `<select>` o `<datalist>`|
|`<optgroup>`|Representa un conjunto de opciones, agrupadas lógicamente dentro de un `<select>`|
|`<datalist>`|Se utiliza junto con la etiqueta `<input>` para proporcionar una lista de opciones `<option>` que ayudan a los usuarios a seleccionar un valor mientras escriben en un campo de entrada `<input>`|
|`<textarea>`|Representa una caja de edición de texto en varias líneas|

**Tabla 4.1.** Etiquetas para la creación de formularios

Ejemplo

```
<form>
    <fieldset>
        <legend>Datos personales</legend>
        <label for="nombre">Nombre y apellidos: </label>
        <input id="nombre" type="text"><br>

        <label for="sexo">Sexo: </label>
        <select id="sexo">
            <!--Etiqueta option-->
            <option value="value1">Hombre</option> 
            <option value="value2" selected>Mujer</option>
        </select><br><br>

        <label>Edad: </label>
        <input type="checkbox" value="20-39"> 20-39
        <input type="checkbox" value="40-59"> 40-59
        <input type="checkbox" value="60-79"> 60-79<br><br>

        <label for="email">Email: </label>
        <input id="email" type="email"><br><br>

        <label for="estudios">Estudios: </label>
        <select id="estudios">
           <optgroup label="Estudios Universitarios">
              <option>Doctorado</option>
              <option>Máster</option>
              <option>Grado</option>
           </optgroup>
           <optgroup label="Ciclo Formativo">
              <option>Grado Superior</option>
              <option>Grado Medio</option>
           </optgroup>
        </select><br><br>

      <label for="navegador">Elige tu navegador favorito: </label>
      <input id="navegador" list="browsers">
        <datalist id="browsers">
            <option value="Chrome">
            <option value="Firefox">
            <option value="Internet Explorer">
            <option value="Opera">
            <option value="Safari">
            <option value="Microsoft Edge">
        </datalist><br><br>

        <label for="mensaje">Escribe tu mensaje: </label>
        <textarea rows="10" cols="50" placeholder="Mensaje" id="mensaje"></textarea>
    </fieldset>  
    <input type="submit" value="Enviar">
</form>
```

### 4.2.1. Etiquetas `<fieldset>` y `<legend>`

Las etiquetas `<fieldset>` y `<legend>` se utilizan para agrupar elementos de formulario relacionados y proporcionar un título o leyenda descriptiva para el grupo.

La etiqueta `<fieldset>` actúa como un contenedor que agrupa campos del formulario. Ejemplo:

```
<form>
<fieldset>
  <legend>Información de contacto</legend>
  <label for="name">Nombre:</label>
  <input type="text" id="name"><br>
  <label for="email">Email:</label>
  <input type="email" id="email"><br>
  <label for="message">Mensaje:</label>
  <textarea id="message"></textarea>
</fieldset>
<fieldset>
  <legend>Intereses</legend>
  <label><input type="checkbox" name="intereses" value="tecnologia"> Tecnología</label><br>
  <label><input type="checkbox" name="intereses" value="musica"> Música</label><br>
  <label><input type="checkbox" name="intereses" value="deportes"> Deportes</label><br>
  <label><input type="checkbox" name="intereses" value="ciencia"> Ciencia</label><br>
  <label><input type="checkbox" name="intereses" value="arte"> Arte</label><br>
</fieldset>   
<input type="submit" value="Enviar">
</form>
```


En este ejemplo, la etiqueta `<fieldset>` envuelve el grupo de elementos de formulario relacionados con la información de contacto. La etiqueta `<legend>` se utiliza como una leyenda o título para el fieldset, proporcionando una descripción del grupo.

El uso de las etiquetas `<fieldset>` y `<legend>` ayuda a mejorar la accesibilidad y usabilidad de los formularios al proporcionar una estructura clara y agrupación visual de campos relacionados. También mejora el estilo general y la organización del formulario.

### 4.2.2. Etiqueta `<label>`

La etiqueta `<label>` ayuda a asociar una descripción de texto con un campo de entrada de formulario, lo que lo hace más accesible y fácil de usar. Ejemplo:

```
<label for="username">Nombre de usuario:</label>
<input type="text" id="username">
```


En este ejemplo, la etiqueta `<label>` se utiliza para crear una etiqueta para el campo de entrada de nombre de usuario. El atributo _for_ de la etiqueta `<label>` especifica con qué elemento de entrada está asociado. En este caso, el valor del atributo _for_ coincide con el atributo _id_ del campo de entrada.

Cuando un usuario hace clic en la etiqueta, el campo de entrada correspondiente se enfoca o activa. Esto mejora la usabilidad y accesibilidad, ya que los usuarios pueden hacer clic en el texto de la etiqueta en lugar de hacer clic directamente en el campo de entrada.

### 4.2.3. Etiqueta `<input>`

La etiqueta `<input>` en HTML se utiliza para crear campos de entrada en un formulario que permiten a los usuarios ingresar datos. El tipo de dato que se ingresa depende del valor del atributo `type` de la etiqueta `<input>`. Veamos algunos ejemplos comunes de cómo se utiliza la etiqueta `<input>` en un formulario:

1.  **Campo de texto**: Permite a los usuarios insertar texto, como su nombre o dirección de correo electrónico.

```
   <input type="text" id="nombre" name="nombre" placeholder="Tu nombre">
```


2.  **Campo de contraseña**: Similar al campo de texto, pero los caracteres insertados se ocultan por asteriscos o puntos para proteger la privacidad de la contraseña.

```
   <input type="password" id="contrasena" name="contrasena" placeholder="Contraseña">
```


3.  **Casilla de verificación (Checkbox)**: Permite a los usuarios seleccionar o deseleccionar una opción.

```
   <input type="checkbox" id="suscripcion" name="suscripcion" value="aceptar">
   <label for="suscripcion">Acepto los términos y condiciones</label>
```


4.  **Botón de radio (Radio Button)**: Permite a los usuarios seleccionar una opción de un conjunto de opciones mutuamente excluyentes.

```
   <input type="radio" id="opcion1" name="opcion" value="opcion1">
   <label for="opcion1">Opción 1</label><br>
   <input type="radio" id="opcion2" name="opcion" value="opcion2">
   <label for="opcion2">Opción 2</label>
```


5.  **Botón (Button)**: Crea un botón que puede utilizarse para enviar un formulario o realizar otras acciones mediante JavaScript.

```
   <input type="button" value="Enviar" onclick="enviarFormulario()">
```


6.  **Campo de correo electrónico**: Ayuda a validar que se inserte una dirección de correo electrónico válida.

```
   <input type="email" id="correo" name="correo" placeholder="Correo electrónico">
```

7.  **Campo de número**: Permite inserar valores numéricos y puede incluir restricciones como mínimo y máximo.

```
   <input type="number" id="edad" name="edad" min="18" max="99" placeholder="Edad">
```

Estos son solo algunos ejemplos de cómo se puede utilizar la etiqueta `<input>` en un formulario HTML. En el punto 4.3 veremos en detalle los atributos del elemento `<input>`.

### 4.2.4. Etiqueta `<button>`

La etiqueta `<button>` en HTML se utiliza para crear un botón. Puede ser utilizado para activar una acción o comportamiento específico al ser clicado.

```
<button>Haz clic</button>
```


También puedes utilizar el atributo _type_ para definir el tipo de botón. Algunos valores comunes para el atributo `type` son:

*   **submit**: Un botón que envía un formulario.
*   **reset**: Un botón que reinicia los valores iniciales de los campos de un formulario.

```
<button type="submit">Enviar</button>
```


### 4.2.5. Diferencias entre `<input>` y `<button>`

Los elementos `<input>` y `<button>` se utilizan para crear botones, pero tienen características distintas que afectan su uso y apariencia.

*   **`<input>`**: Su apariencia es más limitada, ya que solo puede mostrar texto o imágenes y no puede contener otros elementos HTML.
*   **`<button>`**: Es un elemento de botón más versátil que permite incluir contenido HTML, como texto, imágenes o iconos. Esto permite una mayor personalización en la presentación visual.

Por tanto, utiliza `<input>` para botones de formulario con funciones específicas y limitadas, mientras que `<button>` es preferible cuando se necesita más personalización o cuando se requiere incluir contenido HTML adicional.



* Tipo de Elemento: Botón de envío de formulario
  * Etiqueta a utilizar: 
  ```
    <input type="submit">
  ```
  * Descripción: Envía los datos del formulario al servidor.

* Tipo de Elemento: Botón de envío con imagen
  * Etiqueta a utilizar: 
  ```
  <input type="image">
  ```
  * Descripción: Botón que envía el formulario, pero se muestra como una imagen definida en el atributo src.

* Tipo de Elemento: Botón de reinicio de formulario

  * Etiqueta a utilizar: 
  ```
  <input type="reset">
  ```
  * Descripción: Restaura todos los campos del formulario a sus valores iniciales.

* Tipo de Elemento: Botón sin funcionalidad
  * Etiqueta a utilizar: 
  ```
  <input type="button">
  ```
  * Descripción: No envía ni reinicia el formulario, se utiliza para ejecutar scripts de JavaScript.

* Tipo de Elemento: Botón de envío
  * Etiqueta a utilizar: 
  ```
  <button type="submit">
  ```
  * Descripción: Similar al input type="submit", pero permite contenido HTML adicional.

* Tipo de Elemento: Botón de reinicio
  * Etiqueta a utilizar: 
  ```
  <button type="reset">
  ```
  * Descripción: Similar al input type="reset", pero permite contenido HTML adicional.

* Tipo de Elemento: Botón sin funcionalidad
  * Etiqueta a utilizar: 
  ```
  <button type="button">
  ```
  * Descripción: No envía ni reinicia el formulario, se utiliza para ejecutar scripts de JavaScript y permite contenido HTML adicional.


**Tabla 4.2.** Uso frecuente `<input>` y `<button>`

### 4.2.6. Etiqueta `<select>` 

La etiqueta `<select>` en HTML se utiliza para crear un menú desplegable o una lista de opciones seleccionables. Permite al usuario elegir una opción de entre varias disponibles.

Ejemplo básico de cómo utilizar la etiqueta `<select>` junto con la etiqueta `<option>` para crear un menú desplegable:

```
<select>
  <option value="option1">Opción 1</option>
  <option value="option2">Opción 2</option>
  <option value="option3">Opción 3</option>
</select>
```


Cada `<option>` dentro de la etiqueta `<select>` representa una opción en el menú desplegable. El atributo _value_ se utiliza para especificar el valor asociado a cada opción, que se enviará al servidor cuando se envíe el formulario.

También puedes agregar el atributo _selected_ a una opción específica para que se seleccione automáticamente cuando se muestre el menú desplegable:

```
<select>
  <option value="option1">Opción 1</option>
  <option value="option2" selected>Opción 2</option>
  <option value="option3">Opción 3</option>
</select>
```


En este ejemplo, la opción «Opción 2» estará seleccionada de forma predeterminada cuando se muestre el menú desplegable.

La etiqueta `<select>` en HTML también admite el atributo _**multiple**_, que permite al usuario seleccionar múltiples opciones del menú desplegable.

Al agregar el atributo _multiple_ a la etiqueta `<select>`, se permite la selección de varias opciones manteniendo presionada la tecla Ctrl (en Windows) o Cmd (en Mac) mientras se hacen clic en las opciones deseadas. Ejemplo:

```
<select multiple>
  <option value="option1">Opción 1</option>
  <option value="option2">Opción 2</option>
  <option value="option3">Opción 3</option>
</select>
```


La etiqueta `<optgroup>` se utiliza dentro de un elemento `<select>` para agrupar varias opciones relacionadas en una categoría o conjunto. Esto proporciona una organización visual a las opciones dentro de la lista desplegable. La etiqueta `<optgroup>` debe contener una o más etiquetas `<option>` que representan las opciones dentro de ese grupo.

```
<select>
  <optgroup label="Frutas">
    <option value="manzana">Manzana</option>
    <option value="naranja">Naranja</option>
    <option value="platano">Plátano</option>
  </optgroup>
  <optgroup label="Verduras">
    <option value="zanahoria">Zanahoria</option>
    <option value="brocoli">Brócoli</option>
    <option value="espinaca">Espinaca</option>
  </optgroup>
</select>
```


En este ejemplo, hemos creado una lista desplegable con dos grupos: «Frutas» y «Verduras». Cada grupo está definido por la etiqueta `<optgroup>`, que tiene un atributo `label` que especifica el nombre del grupo. Dentro de cada grupo, hemos incluido etiquetas `<option>` que representan las opciones individuales, como «Manzana», «Naranja», «Zanahoria», etc.

Cuando se renderiza en un navegador, esto creará una lista desplegable con las opciones agrupadas visualmente bajo las etiquetas de grupo. Esto facilita que los usuarios encuentren y seleccionen las opciones que desean de manera más organizada.

### 4.2.7. Etiqueta `<datalist>`

La etiqueta `<datalist>` se utiliza junto con la etiqueta `<input>` para proporcionar una lista de opciones predefinidas que ayudan a los usuarios a seleccionar un valor mientras escriben en un campo de entrada `<input>`. Esta etiqueta crea una lista desplegable de sugerencias basadas en las opciones que defines, lo que facilita la entrada de datos y mejora la experiencia del usuario.

A continuación se puede ver un ejemplo de cómo se utiliza la etiqueta `<datalist>`:

```
<label for="frutas">Selecciona una fruta:</label>
<input list="frutas" id="fruta" name="fruta" />

<datalist id="frutas">
  <option value="Manzana"></option>
  <option value="Banana"></option>
  <option value="Naranja"></option>
  <option value="Uva"></option>
  <option value="Pera"></option>
</datalist>
```


En este ejemplo, hemos creado un campo de entrada de texto con la etiqueta `<input>` y le hemos asignado un atributo `list` que corresponde al `id` de la etiqueta `<datalist>`. El `<datalist>` contiene opciones (`<option>`) que representan las sugerencias disponibles para el campo de entrada.

Cuando un usuario comienza a escribir en el campo de entrada, verá una lista desplegable con las opciones del `<datalist>`. Puede seleccionar una de las opciones o seguir escribiendo. Esto es especialmente útil para formularios en los que los usuarios deben elegir una opción de una lista predefinida, como una lista de países o productos.

El uso de `<datalist>` mejora la usabilidad y facilita a los usuarios la entrada de datos, especialmente en dispositivos móviles y pantallas táctiles.

### 4.2.8. Etiqueta `<textarea>`

La etiqueta `<textarea>` en HTML se utiliza para crear un área de entrada de texto de varias líneas. Permite a los usuarios ingresar y editar texto más largo que un solo campo de entrada de texto.

Ejemplo básico de cómo utilizar la etiqueta `<textarea>`:

```
<textarea rows="4" cols="40">
Esto es un textarea con 4 fulas y 40 columnas.
</textarea>
```


En este ejemplo, el atributo **_rows_** define el número de filas visibles del área de texto, mientras que el atributo _**cols**_ establece el número de columnas visibles.

El texto dentro de la etiqueta `<textarea>` se mostrará inicialmente dentro del área de texto y los usuarios podrán editarlo y seleccionarlo.

4.3. Atributos de la etiqueta `<input>`
---------------------------------------

La validación de los datos introducidos por los usuarios en los campos de los formularios es esencial para ofrecer al usuario información sobre los datos que se están solicitando. 

Gracias a los nuevos atributos que se introdujeron en HTML5 no es necesario utilizar JavaScript obligatoriamente para la validación de los campos ya que se validan de forma automática al pulsar en el botón de tipo _submit_.

Veamos los atributos más utilizados para los inputs. Algunos de ellos permiten la validación sin necesidad de usar JavaScript.



* Atributos: type
  * Descripción: Tipo de input: text, password, checkbox, radio, etc.
* Atributos: value
  * Descripción: Valor inicial del input.
* Atributos: readonly
  * Descripción: El input es de solo lectura.
* Atributos: disabled
  * Descripción: El input no se puede modificar.
* Atributos: size
  * Descripción: Cantidad de caracteres visibles en un input. Su valor por defecto es 20. Funciona en los inputs de los siguientes tipos: text, search, tel, url, email, and password.
* Atributos: maxlength 
  * Descripción: Máximo número de caracteres del input.
* Atributos: min / max
  * Descripción: Mínimo y máximo número de caracteres del input.
* Atributos: pattern
  * Descripción: Nos permite indicar un patrón.
* Atributos: placeholder 
  * Descripción: Describe el valor esperado en un campo.
* Atributos: required
  * Descripción: Especifica que es obligatorio completar el input.
* Atributos: autofocus 
  * Descripción: Indica que se hace foco en ese input cuando se carga la página.


**Tabla 4.3.** Atributos para los inputs

[Ver más atributos para los inputs](https://developer.mozilla.org/es/docs/Web/HTML/Elemento/form)

En el siguiente ejemplo, hemos utilizado varios atributos como type, id, name, placeholder, required, minlength, maxlength, min, y max para los campos de entrada. También hemos utilizado el atributo for en las etiquetas `<label>` para asociarlas con los campos correspondientes.

```
<form>
  <label for="name">Nombre:</label>
  <input type="text" id="name" name="name" placeholder="Ingresa tu nombre" required>
  
  <label for="email">Correo electrónico:</label>
  <input type="email" id="email" name="email" placeholder="Ingresa tu correo electrónico" required>
  
  <label for="password">Contraseña:</label>
  <input type="password" id="password" name="password" minlength="8" maxlength="16" required>
  
  <label for="age">Edad:</label>
  <input type="number" id="age" name="age" min="18" max="99" required>
  
  <label for="terms">Acepto los términos y condiciones:</label>
  <input type="checkbox" id="terms" name="terms" required>
  
  <button type="submit">Enviar</button>
</form>
```


En la siguiente tabla se muestran más ejemplos:


|Atributo   |Ejemplo                                           |
|-----------|--------------------------------------------------|
|placeholder|placeholder=”Indica tu nombre”                    |
|required   |required=”true” o required                        |
|pattern    |pattern=”[a-z]{1,5}”                              |
|min        |min=”1”                                           |
|max        |max=”100”                                         |
|step       |step=”2” (saltos en un rango de números: 0, 2, 4…)|
|disabled   |disabled=”true” o disabled                        |
|autofocus  |autofocus=”true” o autofocus                      |


**Tabla 4.4.** Ejemplos de atributos para la validación de campos en los formularios

4.4. Tipos de inputs: atributo type
-----------------------------------

El artributo type de los inputs especifican el tipo de datos que se espera ingresar en el campo. Algunos valores comunes son los siguientes:



* Type: checkbox
  * Description: Casilla de verificación que permite seleccionar o deseleccionar distintos valores.
* Type: color
  * Description: Control para especificar un color; abre un selector de colores cuando está activo.
* Type: date
  * Description: Permite indicar una fecha (año, mes y día, sin hora). Abre un selector de fechas para año, mes y día.
* Type: email
  * Description: Permite insertar un correo electrónico haciendo su validación.
* Type: file
  * Description: Permite seleccionar un archivo.
* Type: image
  * Description: Botón con imagen de tipo submit. La imagen se define en el atributo src.
* Type: month
  * Description: Permite ingresar mes y año.
* Type: number
  * Description: Permite ingresar un número. Muestra un selector y agrega validación predeterminada.
* Type: password
  * Description: Valor oculto. Usado para contraseñas.
* Type: radio
  * Description: Permite seleccionar un valor único entre múltiples opciones.
* Type: range
  * Description: Nos deja ingresar un número cuyo valor exacto no es importante. Se muestra como un widget de rango con un valor predeterminado en el medio. Se utiliza en conjunto con «min» y «max» para definir el rango de valores aceptados.
* Type: search
  * Description: Campo para ingresar cadenas de búsqueda. 
* Type: submit
  * Description: Botón que envía el formulario
* Type: tel
  * Description: Control para ingresar un número de teléfono y agrega validación predeterminada.
* Type: text
  * Description: Control para campo de texto con validación predeterminada.
* Type: time
  * Description: Control para hora.
* Type: url
  * Description: Nos permite ingresar una URL.
* Type: week
  * Description: Control para ingresar una fecha.


**Tabla 4.5**. Tipos de inputs

```
 <form>
  <label for="check">Acepto condiciones</label>
  <input type="checkbox" id="check"><br>
  <label for="color">Elige un color:</label>
  <input type="color" id="color"><br>
  <label for="fecha">Elige una fecha:</label>
  <input type="date" id="fecha"><br>
  <label for="correo">Indica tu correo:</label>
  <input type="email" id="correo"><br>
  <label for="archivo">Selecciona un archivo:</label>
  <input type="file" id="archivo">   <br>
  <label for="archivo">Pincha en la imagen:</label>                                                         
  <input type="image"  src="https://www.eniun.com/wp-content/uploads/eniun-icon-user-experience.svg" alt="Submit" width="38" height="38"><br>
  <label for="mes">Indica el mes:</label>
  <input type="month" id="mes"><br>
  <label for="numero">Selecciona un número:</label>
  <input type="number" id="numero"><br>
  <label for="contrasenya">Indica tu contraseña:</label>
  <input type="password" id="contrasenya"><br>
  <label for="radio">Esto es un radio button:</label>
  <input type="radio" id="radio"><br>
  <label for="rango">Selecciona un número del rango:</label>
  <input type="range" id="rango" min="0" max="100"><br>
  <label for="buscar">Campo de búsqueda:</label>
  <input type="search" id="buscar"><input type="submit" value="Enviar"><br>
  <label for="telefono">Indica tu teléfono:</label>
  <input type="tel" id="telefono"><br>
  <label for="nombre">Indica tu nombre:</label>
  <input type="text" id="nombre"><br>
  <label for="hora">Indica la hora:</label>
  <input type="time" id="hora"><br>
  <label for="url">Indica una URL:</label>
  <input type="url" id="url"><br>
  <label for="semana">Indica la semana:</label>
  <input type="week"><br>
  <input type="button" value="Enviar">
 </form>
```

4.5. Atributo _pattern_ y expresiones regulares
-----------------------------------------------

El atributo _pattern_ nos permite definir nuestras propias reglas para validar el valor de entrada de los campos usando expresiones regulares o _regexp_ (contracción de las palabras inglesas _regular expression_).

Veamos un resumen de algunos de los caracteres que nos ayudan a construir expresiones regulares:


|Clases de caracteres  |                                                       |
|----------------------|-------------------------------------------------------|
|.                     |Cualquier carácter excepto salto de línea              |
|[abc]                 |Cualquiera de los caracteres entre corchetes           |
|[^abc]                |Que NO sea cualquiera de los caracteres entre corchetes|
|[a-g]                 |Cualquier carácter entre a y g (en minúscula)          |
|(a|b)                 |a o b                                                  |
|Anclas                |                                                       |
|^abc                  |Comienzo de una línea                                  |
|abc$                  |Final de una línea                                     |
|Caracteres específicos|                                                       |
|\w\ d \s              |Palabra, dígito, espacio en blanco                     |
|\W \D \S              |Que NO sea palabra, dígito o espacio en blanco         |
|\t \n \r              |Tabulador, salto de línea, retorno de carro            |
|Cuantificadores       |                                                       |
|a* a+ a?              |0 o más veces, 1 o más veces, 0 o 1 vez                |
|a{5} a{2,}            |Solo 5, 2 o más                                        |
|a{1,3}                |Entre 1 y 3                                            |


**Tabla 4.6**. Patrones y expresiones regulares _regexp_

En la siguiente página web puedes ver una referencia de patrones y expresiones regulares. Además, permite la validación de expresiones regulares: [regexr.com](https://regexr.com/)

Expresiones regulares comúnmente utilizadas en atributos HTML:

**Entrada numérica**: Este patrón permite solo valores numéricos en el campo.

```
<input type="number" pattern="[0-9]+">
```


**Patrón personalizado**: Este patrón especifica un formato personalizado donde la entrada debe comenzar con tres letras seguidas de tres dígitos.

```
<input type="text" pattern="[A-Za-z]{3}\d{3}">
```


**Validación de código postal**: Este patrón asegura que el valor de entrada sea un código postal válido de 5 dígitos.

```
<input type="text" pattern="[0-9]{5}">
```


**Validación de fecha (formato AAAA-MM-DD)**: Este patrón valida que el valor de entrada sea una fecha en el formato AAAA-MM-DD. No valida la lógica de los valores de fecha, solo el formato de la cadena.

```
<input type="text" pattern="\d{4}-\d{2}-\d{2}">
```


  
**Validación de nombre de usuario (solo caracteres alfanuméricos):** Este patrón permite solo caracteres alfanuméricos para el nombre de usuario.  

```
<input type="text" pattern="[A-Za-z0-9]+">
```

---
**Ejemplo**

En el siguiente ejemplo se muestra un formulario que solicita los siguientes datos:

*   Nombre de 40 caracteres como máximo y sólo permite letras(mayúsculas y minúsculas).
*   Código postal que admite 5 números.
*   Edad (solo dos dígitos numéricos).

Además, todos los campos son obligatorios y disponen de placeholder. Además, el foco se encuentra en el primer campo. 

```
<h2>Formulario de Contacto</h2>
<form>
<input name="nombre" type="text" placeholder="Nombre" pattern="[a-zA-Z]{1,40}" required autofocus>
<input name="cp" type="text" placeholder="Código postal" pattern="[0-9]{5}" required>	
<input name="edad" type="text" pattern="[0-9]{2}"  placeholder="Edad" required>
<button id="enviar" name="enviar" type="submit">ENVIAR</button>
</form>

```

