---
tags:
  - js
  - interaccion-usuario
---
## Cuadro de diálogo de alerta `alert()`

El método `alert` acepta un parámetro opcional: el texto que se mostrará. El método `alert`  es un método del objeto `window`, pero por conveniencia, se puede utilizar sin necesidad de escribir `window.alert`.

```js
alert("Hello, World!")
window.alert("Hello, World! for the second time");
```

## Cuadro de diálogo de confirmación `window.confirm()`

La diferencia entre `alert` y `confirm` ¿es que el? El cuadro de diálogo `confirm` muestra dos botones, el botón Aceptar y el botón Cancelar. Según el botón que presione el usuario, El método `confirm` devuelve un valor booleano. 

```js
let remove = confirm("Remove all data?");
let message = remove ? "Deleting Data" : "Cancelled"
 
console.log(message);
```

## Cuadro de diálogo de solicitud

El último de los cuadros de diálogo es el `propmt`. Es igual al cuadro de diálogo `confirm`, contiene los botones Aceptar y Cancelar, pero también contiene un campo de texto de una sola línea que permite al usuario ingresar texto.

Acepta un segundo parámetro opcional, que es el valor predeterminado del campo de texto visible en la ventana de diálogo. 

```js
let name = window.prompt("What is your name", "John Doe");
name = name ? name : "anonymous";
let age prompt(`Hello ${name} how old are you?`);
alert(`${name} is ${age} years old`);
```

