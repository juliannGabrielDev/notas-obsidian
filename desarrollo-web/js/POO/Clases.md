---
tags:
  - js
  - poo
---
## Declaración de una clase

Puedes definir una clase usando la palabra clave `class`. Dentro de una clase, se pueden declarar un constructor y métodos.

```js
class Persona {
	constructor(nombre, edad) {
		this.nombre = nombre;
		this.edad = edad;
	}

	saludar() {
		console.log(`Hola soy ${this.nombre} y tengo ${this.edad} años.`)
	}
}

const persona1 = new Persona("Julian", 30);
persona1.saludar(); // Hola, soy Julian y tengo 30 años.
```

## Herencia con Clases

La herencia se realiza utilizando la palabra clave `extends`. Esto permite que una clase hija herede las propiedades y métodos de una clase padre.

```js
class Estudiante extends Persona {
	constructor(nombre, edad, grado) {
		super(nombre, edad);
		this.grado = grado;
	}

	mostrarGrado() {
		console.log(`${this.nombre} está en el grado ${this.grado}.`);
	}
}

const estudiante1 = new Estudiante("María", 25, 10);
estudiante1.saludar();
estudiante1.mostrarGrado();
```

## Métodos estáticos

Los métodos estáticos se utilizan sin necesidad de instanciar la clase. Se declaran con la palabra clave `static`.

```js
class calculadora {
	static sumar(a, b) {
		return a + b;
	}
}

console.log(Calculadora.sumar(3, 7));
```