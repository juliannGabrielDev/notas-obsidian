---
tags:
  - js
  - tipos-datos
---
En JavaScript los **tipos de datos complejos** se gestionan por referencia y permiten agrupar y organizar información de forma dinámica. Esto significa que, al modificar un objeto o array, estás cambiando el mismo espacio de memoria donde se almacena esa información.

>[!IMPORTANT]
>En términos generales, en JavaScript, todo, excepto los primitivos, es un objeto. Por ejemplo **los arrays** también se tratan como un tipo especial de objeto. 
>
>Si queremos asegurarnos de que la variable contiene un array, podemos hacerlo mediante el operador `instanceof`, entre otros.
>`console.log(array  instanceof  Array);`

## Objetos

Los objetos son colecciones de pares clave-valor y son la forma fundamental de estructurar datos complejos.

```js
const persona = {
	nombre: "Juan",
	edad: 30,
	saludar: function() {
		console.log("Hola, soy " + this.nombre);
	}
};

persona.saludar(); // Imprime: Hola, soy Juan
```

## Arrays

Los arrays son listas ordenadas de valores. Puedes almacenar cualquier tipo de dato, incluidos otros arrays u objetos.

```js
const frutas = ["manzana", "banana", "cereza"];
console.log(frutas[1]); // Imprime: banana

frutas.push("naranja");
console.log(frutas); // Imprime: ["manzana", "banana", "cereza", "naranja"]
```

### Funciones

Las funciones en JavaScript son ciudadanos de primera clase y se consideran objetos. Estas te permiten encapsular lógica reutilizable.

### Clases

Las clases ofrecen una sintaxis limpia para crear objetos basados en prototipos, facilitando la creación de estructuras complejas a través de la herencia y la encapsulación.

```js
class Animal {
  constructor(nombre, edad) {
    this.nombre = nombre;
    this.edad = edad;
  }

  presentarse() {
    console.log(`Soy ${this.nombre} y tengo ${this.edad} años.`);
  }
}

const perro = new Animal("Max", 4);
perro.presentarse(); // Imprime: Soy Max y tengo 4 años.
```

### Estructuras Adicionales: Map y Set

**Map** y **Set** son estructuras de datos integradas que permiten manejar colecciones de elementos de forma más especializada.

- **Map** almacena pares clave-valor.
- **Set** almacena valores únicos de cualquier tipo.

```js
// Uso de Map
const mapa = new Map();
mapa.set("clave1", "valor1");
mapa.set("clave2", "valor2");
console.log(mapa.get("clave1")); // Imprime: valor1

// Uso de Set
const conjunto = new Set();
conjunto.add(1);
conjunto.add(2);
conjunto.add(2); // No se añade porque 2 ya existe en el Set
console.log(conjunto); // Imprime: Set { 1, 2 }
```