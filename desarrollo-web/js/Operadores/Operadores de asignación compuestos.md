---
tags:
  - js
  - operadores
---
Al igual que los operadores aritméticos, **los operadores lógicos binarios** se pueden utilizar en combinación con el operador de asignación, creando una asignación lógica AND. `&&=` y una asignación lógica OR `||=`.

Debería ser fácil imaginar cómo funcionan. En el caso del operador AND, podemos comprobarlo con el siguiente ejemplo:

```js
let a = true;
console.log(a); // -> true
a &&= false;
console.log(a); // -> false
```

La instrucción `a &&= false` significa exactamente lo mismo que `a = a && false`.

Podemos preparar un ejemplo similar para las operaciones OR:

```js
let b = false;
console.log(b); // -> false
b ||= true;
console.log(b); // -> true
```

Esta vez, la operación `b ||= true` se interpreta como `b = b || true`.