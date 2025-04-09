---
tags:
  - js
  - tipos-datos
---
En JavaScript existen varios tipos de datos primitivos. **Estos valores son inmutables y se comparan por su valor, no por su referencia**. Conocerlos es esencial para escribir código limpio y predecible.

## Undefined

Representa una variable a la que no se le ha asignado ningún valor.

```js
let valor;
console.log(valor); // Imprime: undefined
```

## Null

Indica la ausencia intencional de cualquier valor. Se usa para señalar que una variable debe estar vacía.

```js
let vacio = null;
console.log(vacio); // Imprime: null
```

## Boolean

## Number

Incluye tanto números enteros como decimales. JavaScript maneja internamente todos los números como de tipo flotante.

```js
let entero = 42;
let decimal = 3.14;
```

## BigInt

Permite representar números enteros muy grandes, que superan el límite del tipo `Number`. Se denota con la letra `n` al final del número.

```js
let granNumero = 9007199254740991n;
```

## String

## Symbol

Crea identificadores únicos que pueden ser utilizados como claves en objetos. Cada symbol es único, incluso si tienen la misma descripción.

```js
let idUnico = Symbol("id");
```