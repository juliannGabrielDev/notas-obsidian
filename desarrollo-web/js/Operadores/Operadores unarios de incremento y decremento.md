---
tags:
  - js
  - operadores
---
Entre los operadores aritméticos, también tenemos a nuestra disposición el incremento unario `++` y decremento `--`, tanto en su versión prefijo como sufijo. 

Estos operadores en la **versión postfija** (es decir, el operador se encuentra en el lado derecho del operando) realizan la operación cambiando el valor de la variable, pero devuelven el valor anterior al cambio.

La **versión prefija** del operador (es decir, el operador se ubica antes del operando) realiza la operación y devuelve el nuevo valor.

```js
let n1 = 10;
let n2 = 10;

console.log(n1); // -> 10
console.log(n1++); // -> 10
console.log(n1); // -> 11

console.log(n2); // -> 10
console.log(++n2); // -> 11
console.log(n2); // -> 11

let n3 = 20;
let n4 = 20;

console.log(n3); // -> 20
console.log(n3--); // -> 20
console.log(n3); // -> 19

console.log(n4); // -> 20
console.log(--n4); // -> 19
console.log(n4); // -> 19
```