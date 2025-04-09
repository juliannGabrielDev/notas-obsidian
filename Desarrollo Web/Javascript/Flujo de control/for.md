---
tags:
  - js
  - flujo-control
---
## Bucle `for`

El bucle `for` es una forma clásica de iterar en JavaScript. Es muy flexible y te permite controlar completamente el proceso de iteración.

```js
for (let i = 0; i < 5; i++) {
  console.log(i);
}
// Salida: 0, 1, 2, 3, 4
```

## Bucle `for...of`

El bucle `for...of` es una forma más moderna y sencilla de iterar sobre objetos iterables, como arrays, strings, maps y sets.

```js
const colores = ['rojo', 'verde', 'azul'];

for (const color of colores) {
  console.log(color);
}
// Salida: rojo, verde, azul
```