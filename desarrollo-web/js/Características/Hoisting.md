---
tags:
  - js
  - variables
---
El **hoisting** es el comportamiento en el que las declaraciones de variables y funciones se "mueven" al comienzo de su contexto de ejecución durante la compilación.

## `var`

Cuando usas `var`, la declaración se eleva, pero **no** la asignación. Por ejemplo:

```js
console.log(miVariable); // Imprime: undefined
var miVariable = 10;
```

## `let` y `const`

>[!CAUTION]
>Las variables declaradas con `let` o `const` también se hoistean, pero permanecen en la zona temporal _dead zone_ hasta que se inicializan, generando un error si se intenta utilizarlas anticipadamente.

```js
console.log(miLet); // ReferenceError: Cannot access 'miLet' before initialization
let miLet = 10
```