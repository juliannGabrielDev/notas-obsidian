---
tags:
  - js
  - estructuras-datos
---
### `.length`

La propiedad de `length` se utiliza para obtener información sobre la longitud (la cantidad de elementos) de la matriz (incluidas las posiciones vacías entre los elementos existentes).

### `.indexOf`

El método se utiliza para buscar en la matriz un valor determinado. Si se encuentra el valor (el elemento está en la matriz), se devolverá su índice (posición). El método devuelve -1 si no se encuentra el elemento. Si hay más de un elemento con el mismo valor en la matriz, se devuelve el índice del primer elemento.

### `.push` Empujar

El método coloca el elemento dado como argumento al final de la matriz. La longitud de la matriz se incrementa en 1 y el nuevo elemento se inserta a la derecha (tiene el índice más grande de todos los elementos).

### `.unshift` Desplazamiento

El método `unshift` funciona de manera similar a `push`, con la diferencia de que se agrega un nuevo elemento al comienzo de la matriz.

### `.pop` Estallido

El método `pop` permite eliminar el último elemento de la matriz. Como resultado de su ejecución, se devuelve el elemento con el índice más grande y, al mismo tiempo, se elimina de la matriz original.

### `.shift` 

El método `shift` funciona de manera similar a `pop`, solo que esta vez eliminamos el elemento del comienzo de la matriz (con el índice `0` ). El método devuelve el elemento eliminado.

### `.reverse`

El método `reverse` invierte el orden de los elementos de la matriz. Como resultado de su llamada, el primer elemento de la matriz original se convertirá en el último, el penúltimo en el último, y así sucesivamente.

### `.slice` Rebanada

El método `slice` permite crear una nueva matriz a partir de elementos seleccionados de la matriz original. Llamar al método no afecta a la matriz original. El método toma uno o dos valores enteros como argumentos.

Las combinaciones básicas son:

- **Un argumento mayor que cero**: se copian todos los elementos desde el índice dado como argumento hasta el final de la matriz;
- **Dos argumentos mayores que cero**: se copia el elemento del índice especificado como primer argumento al elemento especificado como segundo argumento;
- **Dos argumentos, primero positivo, segundo negativo**: se copian todos los elementos desde el índice especificado hasta el final de la matriz, excepto el número especificado de los últimos elementos (por ejemplo, el argumento -3 significa que no copiamos los últimos tres elementos)
- **Un argumento negativo**: el número especificado de los últimos elementos se copian al final de la matriz (por ejemplo, -2 significa que se copian los dos últimos elementos).

```js
let  names  =  ["Olivia",  "Emma",  "Mateo",  "Samuel"];
   
let  n1  =  names.slice(2);
console.log(n1);  //  ->  ["Mateo",  "Samuel"]
   
let  n2  =  names.slice(1,3);
console.log(n2);  //  ->  ["Emma",  "Mateo"]
   
let  n3  =  names.slice(0,  -1);
console.log(n3);  //  ->  ["Olivia",  "Emma",  "Mateo"]
   
let  n4  =  names.slice(-1);
console.log(n4);  //  ->  ["Samuel"]
   
console.log(names);  //  ->  ["Olivia",  "Emma",  "Mateo", "Samuel"]
```

### `.concat`

El método `concat` crea una nueva matriz adjuntando elementos de la matriz dada como argumento a los elementos de la matriz original. El método no cambia ni la matriz original ni la matriz especificada como argumento.

```js
let  names  =  ["Olivia",  "Emma",  "Mateo",  "Samuel"];
let  otherNames  =  ["William",  "Jane"];
let  allNames  =  names.concat(otherNames);
   
console.log(names);  //  ->  ["Olivia",  "Emma",  "Mateo", "Samuel"]
console.log(otherNames);  //  ->  ["William",  "Jane"]
console.log(allNames);  //  ->  ["Olivia",  "Emma",  "Mateo", "Samuel",  "William",  "Jane"]
```