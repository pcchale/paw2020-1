# Trabajo Práctico Nº1: Introducción al maquetado

La parte teórica del TP se encuentra en la siguiente sección, dentro de este mismo README.

## Teoría

### 1. ¿Qué es un lenguaje de marcado? ¿Cuál es su utilidad? ¿Qué es un tag? ¿Qué es un atributo?

Es un lenguaje de marcado. Se utiliza para darle formato a un texto haciendo uso de tags (o etiquetas). Dicho texto etiquetado luego será interpretado por algún software (usualmente un navegador, o browser), y haciendo uso de sus etiquetas podrá representar la información contenida de distintas maneras, mucho mas amigables al ojo humano. Cada etiqueta tiene un uso distinto, y su correcta implementación facilita la comprensión y navegación del usuario.

Un tag es un segmento de texto encerrado entre los símbolos menor y mayor <>, y definido de antemano para ser representado por un navegador u aplicación de una forma conocida. Casi todo tag tiene su par, con una versión de si mismo que indica el fin de un segmento "taggeado" o etiquetado; por ejemplo en HTML, el tag utilizado para indicar la existencia de párrafos `<p>`, que tiene su par en `</p>`, que indica el fín del mismo.

Los tags pueden admitir atributos, que indican la forma en que dicho tag será interpretado. Estos son incluidos posteriormente al nombre de la etiqueta, encerrado por los mismos símbolos de menor y mayor. Por ejemplo, cuando se incluye una imagen:

```html
    <img src="imagenes/imagen1.png" title="Esta es la primer imagen" alt="Imagen 1">
```

Los campos src, title y alt son atributos de la misma, que indican donde se encuentra dicha imagen, que texto mostrar al pasar el mouse por arriba de la misma, y que texto mostrar cuando la imagen no puede ser descargada (o cuando se usan herramientas de accesibilidad) respectivamente.

### 2. ¿Cuál es la utilidad de HTML? ¿Qué conjunto mínimo de tags debe contener un documento
### elaborado en este lenguaje? Describa brevemente su utilidad.

El HTML o Hypertext Markup Language es un lenguaje de marcado que, utilizando etiquetas como fue explicitado anteriormente, permite la elaboración de páginas web que sean mas que solo texto plano.

Como mínimo, un documento HTML debe incluir:
* `<!DOCTYPE HTML>` , que marca el inicio del documento, lenguate a usar y su versión (estandar HTML5).
* `<html> </html>`. Estas indican el inicio y fin del uso de tags que responden al lenguage HTML propiamente dicho, y enmarcan la totalidad del documento.
* `<head> </head>`, que corresponden al encabezado del documento. En este se especifica (entre otros) el siguiente tag necesario;
* `<title> </title>`. Este define el título a mostrar en la ventana del browser que muestre nuestro documento.
* `<body> </body>`, que indica una sección fuera del head en la cual se encuentra el cuerpo del documento. 

Una estructura básica responde al siguiente esquema:

```html
<!DOCTYPE HTML>
<html>
    <head>
	    <title>Título de la página</title>
	</head>
	<body>
		<p>Contenido de un párrafo, dentro del cuerpo del documento</p>
	</body>
</html>
```

### 3. ¿Cuál es la utilidad e importancia de los enlaces o links entre páginas? ¿Qué significa hipertexto?
### ¿Un link solo puede apuntar a otra página? ¿Qué importancia tiene esto último?

Los enlaces entre páginas permiten que uno se mueva entre estas, posibilitando así "navegar" la web, o al menos lo que los creadores de dichas páginas deseen mostrarnos. Estos enlaces son llamados hipertexto, en referencia al hecho que son texto que contiene otro texto (o en este caso, un enlace a uno). 

Los enlaces pueden apuntar a muchos tipos de recursos distintos y no solo a otras páginas, como puede ser imágenes, videos, archivos, etc. Esto es lo que vuelve a la web tan rica en cuanto a las posibilidades que permite en tanto a compartir información.

### 4. ¿Cómo funcionan los tags audio y video?

Los tags de audio y video tienen una estructura muy similar entre ellos. Como atributo de ambos tags, "controls" indica al browser que debe representar su panel de controles de audio o video por defecto, según cual tag se use. En el caso particular del tag video también se hace uso de los atributos width y height para definir el tamaño con el cual representar el video a mostrar.

Ambos hacen uso del tag `<source>` con los atributos src y type. El primero indica el camino relativo del archivo a reproducir, mientras que el segundo indica el formato del mismo.

Cualquier texto que exista entre los tags `<audio> </audio>` y `<video> </video>` será mostrado en caso que el browser no soporte el uso de dichos tags.

A modo de ejemplo: 

```html
<audio controls>
    <source src="horse.ogg" type="audio/ogg">
    <source src="horse.mp3" type="audio/mpeg">
    Tu broswer no soporta el tag audio.
</audio> 
```

```html
 <video width="320" height="240" controls>
  <source src="movie.mp4" type="video/mp4">
  <source src="movie.ogg" type="video/ogg">
  Tu broswer no soporta el tag video.
</video> 
```

### 5. ¿Qué es el Rendering Engine de un Browser? ¿Cuál es el que utiliza cada uno de los 5 browsers más conocidos (Chrome, Firefox, Safari, IE-Edge, Opera)? ¿Cuál es la importancia de conocer cada uno de ellos en la construcción de un sitio?

Comunmente llamado "motor" en español, el Rendering Engine de un Browser es el software que, habiendo leído un documento HTML, hace uso de los tags indicados en su interior para darnos una representación visual del contenido del documento.

Los siguientes son los motores mas utilizados:

* Chrome: Blink
* Firefox: Gecko
* Safari: WebKit
* IE: Trident
* Edge: Blink (desktop), EdgeHTML (Applicación UWP únicamente)
* Opera: Blink

Aunque hoy en día son bastante parejos, cada motor tiene sus propias funciones o forma de hacer cosas que lo diferencian de los otros, y ventajas o desventajas de performance para ciertas funciones respecto el resto de los motores. Uno debe conocer los puntos fuertes y débiles de cada uno para seleccionar cual priorizar a la hora de crear un sitio web, en caso de ser necesario.


## Práctica

### 6. Dibujar el Wireframe correspondiente a la página principal de lujan.gob.ar y en función a este desarrollar el código HTML5 correspondiente. 

#### Nota: Realizar una captura en imagen del sitio a fin de poder corregir contrastando con lo que muestra el sitio ese día ya que puede variar.

El ejercicio 6 se encuentra dentro de la carpeta [Ejercicio_6](https://github.com/matalmazan/paw2020-1/tree/master/Ejercicio_6).

Dentro de la misma pueden verse:
* [La captura de la página web](https://github.com/matalmazan/paw2020-1/blob/master/Ejercicio_6/Screenshot_2020-04-02%20Municipalidad%20de%20Luj%C3%A1n%20%E2%80%93%202020.jpg),
* [El wireframe de la misma](https://github.com/matalmazan/paw2020-1/blob/master/Ejercicio_6/Wireframe%20-%20lujan.gob.ar.pdf), 
* y [el código HTML que intenta representarla](https://github.com/matalmazan/paw2020-1/blob/master/Ejercicio_6/Ejercicio_6.html)

### 7. Elabore en HTML5 una página que contenga su currículum vítae, respetando la estructura que se muestra a continuación. Tenga en cuenta que los elementos subrayados son enlaces a páginas web o a direcciones de correo electrónico y que la foto debe ser un enlace a la propia imagen. Determine qué tags con qué atributos son necesarios en cada caso.

Referirse al ejercicio 7 del [PDF del Trabajo Práctico N.º1](https://github.com/matalmazan/paw2020-1/blob/master/PAW_TP1_HTML.pdf) para ver el modelo de currículum vitae.

La respuesta al ejercicio 7 se encuentra dentro de la carpeta [Ejercicio_7](https://github.com/matalmazan/paw2020-1/tree/master/Ejercicio_7). Allí encontraran:

* Un documento HTML que representa al CV de ejemplo
* La/s imagen/es a usar para foto de perfil y otros para el mismo. Las imágenes no incluidas son consideradas decorativas


### 8. Elabore el código necesario para representar la siguiente tabla:

Referirse al último ejercicio del [PDF del Trabajo Práctico N.º1](https://github.com/matalmazan/paw2020-1/blob/master/PAW_TP1_HTML.pdf) para ver la tabla.

La respuesta al ejercicio 8 se encuentra dentro de la carpeta [Ejercicio_8](https://github.com/matalmazan/paw2020-1/tree/master/Ejercicio_8). En la misma se verá:

* Un documento HTML que representa la tabla dada
