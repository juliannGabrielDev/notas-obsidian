---
tags:
  - js
  - estructuras-datos
---
El método `forEach` es una manera eficiente y legible de recorrer arrays en JavaScript. Ejecuta una función proporcionada una vez por cada elemento del array.

## Sintaxis básica

La sintaxis es sencilla: recibe como argumento una **función de callback** que se ejecuta en cada elemento.

```js
const numeros = [1, 2, 3, 4, 5];

numeros.forEach(function(numero) {
	console.log(numero);
});
```

## Uso con funciones flecha

Puedes simplificar aún más el código utilizando funciones flecha.

```js
numeros.forEach(numero => console.log(numero));
```

## Acceso a índices

Si necesitas acceder a los índices de los elementos, el `forEach` proporciona un segundo parámetro en la función de callback.

```js
numeros.forEach((numero, index) => {
	console.log(`Índice: ${indice}, Valor: ${numero}`);
});
```

## Limitaciones

- **No devuelve un nuevo array**: A diferencia de otros métodos como `map`, `forEach` no crea un nuevo array.
    
- **No se puede interrumpir**: A diferencia de un bucle `for`, no puedes detener la ejecución de `forEach` con una instrucción como `break`.