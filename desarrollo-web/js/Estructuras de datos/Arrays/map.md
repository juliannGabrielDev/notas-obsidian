---
tags:
  - js
  - estructuras-datos
---
`map` es un método de los array que permite transformar cada elemento de un array y crear un nuevo array con los resultados. No modifica el array original.

## Sintaxis y Uso Básico

La sintaxis básica de `map` es:

```js
const nuevoArray = array.map((elemento, indice, array) => {
	// Retorna el nuevo valor para el elemento transformado.
});
```

Por ejemplo, para duplicar los valores de un array:

```js
const numeros = [1, 2, 3, 4, 5];
const duplicados = numeros.map(num => num * 2);

console.log(duplicados); // [2, 4, 6, 8, 10]
```

## Ejemplo con Más de un Parámetro

El callback recibe tres argumentos: el `elemento` actual, su `índice` y el `array` completo. En este ejemplo, vamos a concatenar el índice a cada número:

```js
const numeros = [1, 2, 3, 4, 5];
const transformados = numeros.map((num, index, arr) => {
  console.log(`Procesando ${num} del array ${arr}`);
  return `${num} en la posición ${index}`;
});

console.log(transformados);
// Salida: 
// ["1 en la posición 0", "2 en la posición 1", "3 en la posición 2", "4 en la posición 3", "5 en la posición 4"]
```

## Características Clave

- **Inmutabilidad:** Crea un nuevo array, sin modificar el original.
- **Función de transformación:** Permite transformar cada elemento según algún criterio o proceso.
- **Encadenable:** Puedes combinar `map` con otros métodos como `filter` o `reduce`.