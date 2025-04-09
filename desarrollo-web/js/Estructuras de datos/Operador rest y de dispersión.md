---
tags:
  - js
  - estructuras-datos
---
## Rest

El operador **rest** representado por `...`, permite recopilar una cantidad variable de argumentos en un array. Se suele utilizar en la declaración de funciones para capturar parámetros adicionales o en la destructuración de arrays.

### Uso en Funciones

Al definir una función, puedes usar el operador rest para recoger todos los argumentos restantes en un solo array. Esto es especialmente útil cuando no conoces de antemano cuántos argumentos recibirás.

```js
function sumar(...numeros) {
  // 'numeros' es un array con todos los argumentos pasados a la función
  return numeros.reduce((acum, num) => acum + num, 0);
}

console.log(sumar(1, 2, 3));       // 6
console.log(sumar(10, 20, 30, 40)); // 100
```

### Uso en Destructuring

El operador rest también es útil en la destructuración de arrays para separar algunos elementos del resto.

```js
const numeros = [10, 20, 30, 40, 50];
const [primero, segundo, ...resto] = numeros;

console.log(primero); // 10
console.log(segundo); // 20
console.log(resto);   // [30, 40, 50]
```


---
## Dispersión

El operador de dispersión se representa con `...` y permite expandir elementos de arrays, objetos u otros iterables de forma sencilla. Es muy útil para combinar, copiar o pasar datos como argumentos.

### Unir arrays y objetos 

**Arrays**:
```js
const frutas = ["Naranja", "Manzana", "Pera"];
const bayas = ["fresa", "arándano"];

const frutasYBayas = [...fruits, ...bayas];
```

**Objetos**:
```js
const volador = { alas: 2 }
const carro = { ruedas: 4 }

const autoVolador = { ...volador, ...carro }
console.log(autoVolador);

// { alas: 2, ruedas: 4 }
```

### Otros usos

- Convertir String a Array
- Copiar arrays y objetos completos
- Añadir nuevos miembros a los arrays sin .push()