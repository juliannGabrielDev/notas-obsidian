---
tags:
  - js
  - operadores
---
Mientras los operandos sean del tipo booleano, podemos ver fácilmente lo que se devolverá. Pero esos operadores también se pueden usar con diferentes tipos de datos.

```js
let nr = 0;
let year = 1970;
let name = "Alice";
let empty = "";
 
console.log(!nr); // -> true
console.log(!year); // -> false
console.log(!name); // -> false
console.log(!empty); // -> true
 
console.log(!!nr); // -> false
console.log(!!name); // -> true
```

Esto es ligeramente diferente para los operadores lógicos binarios (es decir, AND y OR). No devuelven un valor booleano. En realidad, devuelven su primer o segundo operando.

```js
console.log(true && 1991); // -> 1991
console.log(false && 1991); // -> false
console.log(2 && 5); // -> 5
console.log(0 && 5); // -> 0
console.log("Alice" && "Bob"); // -> Bob
console.log("" && "Bob"); // -> empty string
 
 
console.log(true || 1991); // -> true
console.log(false || 1991); // -> 1991
console.log(2 || 5); // -> 2
console.log(0 || 5); // -> 5
console.log("Alice" || "Bob"); // -> Alice
console.log("" || "Bob"); // -> Bob
```

Ambos operadores también utilizan **la evaluación de cortocircuito** .

Entonces, si el primer operando de **AND** es `false`, será devuelto y no se realizará ninguna otra verificación.

Por el contrario, si el primer operando de **OR** es `true`, se devolverá y no se realizará ninguna otra comprobación.