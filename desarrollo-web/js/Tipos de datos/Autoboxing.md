---
tags:
  - js
  - tipos-datos
---
En JavaScript, el **autoboxing** es un mecanismo que permite que los valores de tipo primitivo (como `number`, `string`, `boolean`, etc.) se conviertan automáticamente en objetos correspondientes (como `Number`, `String`, `Boolean`, etc.) cuando se necesitan métodos o propiedades de objetos. Esta conversión es automática y es gestionada internamente por JavaScript.

```js
let num = 42;
let str = "Hola";

// Aunque 'num' es un tipo primitivo, podemos invocar métodos como si fuera un objeto.
console.log(num.toString()); // "42"
console.log(str.toUpperCase()); // "HOLA"
```

JavaScript automáticamente crea un objeto `Number` para `num` y un objeto `String` para `str`, permitiendo que se usen los métodos `toString()` y `toUpperCase()`. Luego, después de ejecutar el código, JavaScript destruye estos objetos, volviendo a los valores primitivos.