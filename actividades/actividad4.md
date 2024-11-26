4\. Crea un formulario de registro
-----------------------------------------------------------

Crea una página de registro en HTML que recoja información detallada de los usuarios. La página debe contener los siguientes campos:

**Información Personal:**

*   Nombre (Campo de texto, requerido)
*   Apellido (Campo de texto, requerido)
*   Fecha de Nacimiento (Campo de fecha, requerido)
*   Género (Selector de tipo radio: Masculino, Femenino, Otro, requerido)

**Información de Contacto:**

*   Dirección de Correo Electrónico (Campo de correo electrónico, requerido)
*   Número de Teléfono (Campo de teléfono, requerido)
*   Dirección (Campo de texto de varias líneas)

**Información de Cuenta:**

*   Nombre de Usuario (Campo de texto, requerido)
*   Contraseña (Campo de contraseña, requerido)
*   Confirmación de Contraseña (Campo de contraseña para confirmar, requerido)

**Preferencias:**

*   Seleccionar un Color Favorito (Selector de tipo select: Rojo, Azul, Verde, Amarillo)
*   Aceptar Términos y Condiciones (Selector de tipo checkbox, requerido)

Utiliza etiquetas `fieldset` y `legend` para agrupar y describir secciones de formulario. Asegúrate de que los campos marcados como «requeridos» deben ser completados antes de enviar el formulario. Enlaza cada etiqueta `<label>` con su campo de entrada correspondiente utilizando los atributos `for` e `id` para mejorar la accesibilidad. Al final del formulario, incluye un botón donde pulsar para enviar la información completada por el usuario al servidor.