---
tags:
  - js
  - estructuras-datos
---
`filter` es un método de arrays que permite crear un nuevo array con todos los elementos que cumplen una condición especificada en una función callback.

## ¿Cómo funciona?

Recorre cada elemento del array y evalúa la condición. Si el callback retorna `true`, el elemento se incluye en el nuevo array, si devuelve `false`, se omite.

```js
const nuevoArray = array.filter((elemento, indice, array) => {
	// Retorna true o false según la condición
});
```

## Ejemplo

Imagina que quieres obtener todos los números pares de un array:

```js
const numeros = [1, 2, 3, 4, 5, 6];

const pares = numeros.filter(numero => numero % 2 == 0);

console.log(pares); // [2, 4, 6]
```

## Más Uso del Callback

Además del elemento actual, el callback acepta dos parámetros adicionales: el índice y el array original.

```js
const palabras = ['manzana', 'pera', 'banana', 'cereza'];

const palabrasLargas = palabras.filter((palabra, indice, array) => {
    console.log(`Procesando el índice ${indice}: ${palabra}`);
    console.log(array.length)
    return palabra.length > 5;
});

console.log(palabrasLargas); // ['manzana', 'banana', 'cereza']
```

