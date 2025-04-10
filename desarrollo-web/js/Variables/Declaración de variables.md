---
tags:
  - js
  - variables
---
Para las declaraciones, usamos las palabras clave `var` o `let` para las variables y `const` para las constantes.

>[!TIP]
>Una de las diferencias entre `var` y `let` es que `let` **nos impide declarar otra variable con el mismo nombre** (se genera un error). El uso de `var` le permite volver a declarar una variable, lo que puede conducir a errores en la ejecución del programa.

```js
var height;
var height;
console.log(height); /* -> undefined */
```

Al declarar con `let`, el intérprete comprueba si dicha variable ya ha sido declarada, independientemente de si `let` o `var` se utilizan en la declaración anterior.

```js
let height;
let height; /* -> Uncaught SyntaxError: Identifier 'height' has already been declared */
console.log(height);
```

Por lo tanto, use `let` para declarar variables, aunque solo sea porque no desea volver a declarar accidentalmente una variable.