## Atributos de validación

La **validación de formularios HTML** es un conjunto de **atributos** que podemos añadir a las entradas de los formularios para realizar una validación automática en nombre del usuario.

- [[#required|required]]
- [[#maxlength|maxlength]]
- [[#minlength|minlength]]
- [[#min y max|min y max]]
- [[#multiple|multiple]]
- [[#pattern|pattern]]

## required

Denota una entrada obligatoria que el usuario no puede dejar vacía.

```html
<input type="text" id="firstName" name="firstName" required>
```

## maxlength

El número máximo de caracteres que se pueden introducir para un campo específico.

```html
<input type="text" id="description" name="description" maxlength="50">
```

## minlength

Especifica la longitud mínima de una entrada de texto.

```html
<input type="password" id="password" name="password" minlength="8">
```

## min y max

Determinan los valores mínimo y máximo permitidos para un campo de entrada. Suelen aplicarse a entradas de texto numéricas, entradas de rango o fechas.

```html
<input type="number" id="quantity" name="quantity" min="1" max="10">
<input type="range" id="volume" name="volume" min="1" max="100">
```

## multiple

Indica que el usuario puede introducir más de un valor en un mismo campo de entrada. Este atributo sólo puede utilizarse para los tipos de entrada **correo electrónico** y **archivo**.

```html
<input type="file" id="gallery" name="gallery" multiple>
```

## pattern

Define un patrón particular que el valor de un campo de entrada debe cumplir para ser considerado válido. Este atributo espera una expresión regular para especificar el patrón. Funciona con los tipos de entrada **texto**, **fecha**, **búsqueda**, **URL**, **tel**, **correo electrónico** y **contraseña**. Por ejemplo, puede restringir los números de teléfono para que sólo sean del Reino Unido. 

```html

<input type="tel" id="phone" name="phone" pattern=”^(?:0|\+?44)(?:\d\s?){9,10}$”>

```