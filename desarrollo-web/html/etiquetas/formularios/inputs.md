# Inputs

La mayoría de las entradas van de la mano con la etiqueta label para las mejores prácticas de accesibilidad.

- [[#button|button]]
- [[#checkbox|checkbox]]
- [[#radio|radio]]
- [[#submit|submit]]
- [[#text|text]]
- [[#password|password]]
- [[#date|date]]
- [[#datetime-local|datetime-local]]
- [[#email|email]]
- [[#file|file]]
- [[#hidden|hidden]]
- [[#image|image]]
- [[#number|number]]
- [[#range|range]]
- [[#reset|reset]]
- [[#search|search]]
- [[#time|time]]
- [[#tel|tel]]
- [[#url|url]]
- [[#week|week]]
- [[#month|month]]

## button

Muestra un botón en el que se puede hacer clic y se utiliza sobre todo en formularios HTML para activar un script cuando se hace clic en él.

```html
<button onclick="alert('Are you sure you want to continue?')">
	<img src="https://yourserver.com/button_img.jpg"
		alt="Submit the form" height="64" width="64">
 </button>
```

## checkbox

Define una casilla de verificación que permite seleccionar o de-seleccionar valores individuales.

```html
<input type="checkbox" id="dog" name="dog" value="Dog">
<label for="dog">I like dogs</label>
<input type="checkbox" id="cat" name="cat" value="Cat">
<label for="cat">I like cats</label>
```
## radio

Muestra un botón de radio que permite seleccionar un único valor entre varias opciones. Normalmente se presentan en grupos de radio, que es una colección de botones de radio que describen un conjunto de opciones relacionadas que comparten el mismo atributo "nombre".

```html
<input type="radio" id="light" name="theme" value="Light">
<label for="light">Light</label>
<input type="radio" id="dark" name="theme" value="Dark">
<label for="dark">Dark</label>
```

## submit

Muestra un botón de envío para enviar todos los valores de un formulario HTML a un manejador de formularios, normalmente un servidor.

```html
<form action="myserver.com" method="POST">
	…
	<input type="submit" value="Submit" />
</form>
```
## text

Define un campo de texto básico de una sola línea en el que un usuario puede introducir texto.

```html
<label for="fname">First name:</label>
<input type="text" id="fname" name="fname">
```

## password

Define un campo de texto de una sola línea cuyo valor queda oculto, adecuado para información sensible como contraseñas.

```html
<label for="pwd">Password:</label>
<input type="password" id="pwd" name="pwd">
```

## date

Muestra un control para introducir una fecha sin hora (año, mes y día).

```html
<label for="dob">Date of birth:</label>
<input type="date" id="dob" name="date of birth">
```

## datetime-local

Define un control para introducir una fecha y una hora, incluyendo el año, el mes y el día, así como la hora en horas y minutos.

```html
<label for="birthdaytime">Birthday (date and time):</label>
<input type="datetime-local" id="birthdaytime" name="birthdaytime">
```

## email

Define un campo para una dirección de correo electrónico. Es similar a una entrada de texto sin formato, con el añadido de que se valida automáticamente cuando se envía al servidor.

```html
<label for="email">Enter your email:</label>
<input type="email" id="email" name="email">
```

## file

Muestra un control que permite al usuario seleccionar y cargar un archivo desde su ordenador. Para definir los tipos de archivos permitidos puede utilizar el atributo "aceptar". Además, para permitir la selección de varios archivos, añada el atributo "múltiple".

```html
<label for="myfile">Select a file:</label>
<input type="file" id="myfile" name="myfile">
```
## hidden

Define un control que no se muestra pero cuyo valor se sigue enviando al servidor.

```html
<input type="hidden" id="custId" name="custId" value="3487">
```
## image

Define una imagen como botón gráfico de envío. Debe utilizar el atributo "src" para señalar la ubicación de su archivo de imagen.

```html
<input type="image"src="submit_img.png" alt="Submit" width="48" height="48">
```
## number

Define un control para introducir un número.

```html
<input type="number" id="quantity" name="quantity" min="1" max="5">
```
## range

Muestra un widget de rango para especificar un número entre dos valores. El valor exacto, sin embargo, no se considera importante.

```html
<input type="range" id="volume" name="volume" min="0" max="10">
```

## reset

Muestra un botón que restablece el contenido del formulario a sus valores por defecto.

```html
<input type="reset">
```

## search

Define un campo de texto para introducir una consulta de búsqueda. Funcionalmente son idénticos a las entradas de texto, pero pueden tener un estilo diferente según el navegador.

```html
<label for="gsearch">Search in Google:</label>
<input type="search" id="gsearch" name="gsearch">
```

## time

Muestra un control para introducir un valor horario en horas y minutos, sin zona horaria.

```html
<label for="appt">Select a time:</label>
<input type="time" id="appt" name="appt">
```

## tel

Define un control para introducir un número de teléfono. 

```html
<label for="phone">Enter your phone number:</label>
<input type="tel" id="phone" name="phone" pattern="[+]{1}[0-9]{11,14}">
```

## url

Muestra un campo para introducir una URL de texto.

```html
<label for="homepage">Add your homepage:</label>
<input type="url" id="homepage" name="homepage">
```

## week

Define un control para introducir una fecha consistente en un número de semana-año y un año, sin zona horaria. Tenga en cuenta que se trata de un tipo más reciente que no es compatible con todos los navegadores.

```html
<label for="week">Select a week:</label>
<input type="week" id="week" name="week">
```
## month

Muestra un control para introducir un mes y un año, sin zona horaria. Tenga en cuenta que se trata de un tipo más nuevo que no es compatible con todos los navegadores.

```html
<label for="bdaymonth">Birthday (month and year):</label>
<input type="month" id="bdaymonth" name="bdaymonth" min="1930-01" value="2000-01">
```