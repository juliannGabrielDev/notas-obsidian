---
tags:
  - js
  - operadores
---
También existen varios operadores aritméticos unarios (que operan sobre un solo operando). Entre ellos se encuentran el signo más ` + `y menos ` - ` operadores.

Ambos operadores convierten operandos al tipo Número, mientras que el operador menos además lo niega.

```js
let str = "123";
let n1 = +str;
let n2 = -str;
let n3 = -n2;
let n4 = +"abcd";
 
console.log(`${str} : ${typeof str}`); // -> 123 : string
console.log(`${n1} : ${typeof n1}`); // -> 123 : number
console.log(`${n2} : ${typeof n2}`); // -> -123 : number
console.log(`${n3} : ${typeof n3}`); // -> 123 : number
console.log(`${n4} : ${typeof n4}`); // -> NaN : number
```