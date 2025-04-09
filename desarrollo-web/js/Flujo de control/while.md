---
tags:
  - js
  - flujo-control
---
El bucle `while` es uno de los bucles que normalmente utilizamos cuando no sabemos exactamente cuántas veces debe repetirse algo, pero sí sabemos cuándo parar. Ejemplo:

```js
let n = 0;
while(n < 91) {
    console.log(n); // -> 0, 10, 20, 30, 40, 50, 60, 70, 80, 90
    n += 10;
}
```

Esta vez, la decisión de finalizar el bucle la tomará el usuario respondiendo la pregunta realizada durante cada iteración del bucle (usaremos el diálogo `confirm` que presentamos recientemente).

```js
let terminado = false;
let contador = 1;

while (terminado != true) {
    let continuarBucle = confirm(`[${contador}] ¿Continuar con el bucle?`);
    terminado = continuarBucle === true ? false : true;
    contador = contador + 1;
}

```

Versión simplificada:

```js
let terminado = false;
let contador = 1;
 
while (!terminado) {
    terminado = !confirm(`[${contador++}] ¿Continuar con el bucle?`);
}
```