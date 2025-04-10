---
Fecha: 2024-12-25
Categoría: La entrevista de codificación
tags:
  - front-end
  - curso-9
  - modulo-1
---
## **Introducción**
---
Una herramienta valiosa en la caja de herramientas de un programador es el pseudocódigo. En esta lectura, aprenderá por qué debe utilizar el pseudocódigo, cuándo debe utilizarse y cómo escribir pseudocódigo.

## **1 ¿Por qué debe utilizar el pseudocódigo?**
---
El pseudocódigo es un primer paso legítimo cuando se empieza a idear una solución. El pseudocódigo es una representación de alto nivel de ideas escritas de forma que parezcan código. Fundamentalmente puede ser una ayuda para destacar por sí mismo qué elementos debe incluir un programa.

Cada línea le dará un momento para detenerse y considerar qué se necesita para lograr un resultado determinado. Al escribir una aplicación, una decisión tomada en la etapa 3 podría influir en la forma en que debería codificarse la etapa 6. Cada etapa tiene un elemento de restricción que informa de cómo se completará una etapa posterior.

Considere que está escribiendo una aplicación que debe almacenar datos en el paso 3. Se decide por un array antes de continuar. En el paso 6, se da cuenta de que se requieren varias búsquedas para una aplicación. Mientras escribe el pseudocódigo, es fácil volver a visitar el paso 3 y cambiar la estructura de datos por algo más compatible con el paso 6, como utilizar un diccionario en lugar de una matriz. Los cambios ligeros podrían aumentar su sobrecarga si ya se ha iniciado una aplicación porque alteran el funcionamiento de los pasos 4 y 5.

## **2 ¿Cuándo debe escribir pseudocódigo?**
---
- Como principiante, al trazar el progreso previsto de su planteamiento.

- Como programador experimentado, cuando intente lidiar con un problema complejo.

- Si está intentando transmitir un concepto a un público influyente, como un equipo o clientes potenciales.

- Si está señalando su trabajo a futuros programadores que puedan mantener el código o la aplicación que usted escribió.

- En una entrevista, al demostrar su capacidad para razonar un problema.

## **3 Cómo escribir pseudocódigo**
---
No hay una forma fija de escribir pseudocódigo. Cada organización puede tener su propia norma. En general, se puede decir que el pseudocódigo puede considerarse como cualquier representación textual que esboce el funcionamiento de un programa.

Considere cómo representar el reto FizzBuzz utilizado para probar la capacidad de los candidatos para razonar en código:

_Escriba un programa en un lenguaje dado que itere sobre los números del 1 al 40. Imprima un número para cada número excepto para los múltiplos de tres, en cuyo caso emita Fizz. Para los múltiplos de cinco, imprima Buzz, y para los múltiplos de 3 y 5 imprima FizzBuzz._

Podría empezar representando cada requisito como una línea de pseudocódigo:

```
FOR number 1 to 40
	IF multiple of 3
		output(Fizz)
	IF multiple of 5
		output(Buzz)
	IF multiple of 3 and 5
		output(number)
```

La clave de esta tarea es saber cómo ordenar la declaración condicional. La línea 1 indica que habrá una iteración. En este caso, una sangría demuestra que las ocho líneas de código siguientes forman parte de esta iteración. Como alternativa, se podría haber añadido el siguiente bloque:

```
START FOR LOOP

#code

END FOR LOOP
```

Está claro que hay tres sentencias condicionales y luego una cláusula catchall `else`. Es posible visualizar el resultado del código observando el pseudocódigo. La sentencia `else` funcionará bien, sólo debe imprimir los no múltiplos de 3 y 5, pero hay un problema con la forma en que el código manejará el número 15, imprimiendo una instancia de Fizz, Buzz y FizzBuzz. 

```
FOR number 1 to 40
	IF multiple of 3 and 5
		output(FizzBuzz)
	ELSE IF multiple of 3
		output(Fizz)
	ELSE IF multiple of 5
		output(Buzz)
	ELSE 
		output(nummber)
```

Examinar la primera instancia de la pregunta como pseudocódigo le permite detectar dónde pueden estar los problemas. Visualmente, es mucho más fácil ver cómo deben organizarse las sentencias condicionales. En primer lugar, el quid de la cuestión es en qué orden deben colocarse las sentencias condicionales y utilizar sentencias condicionales excluyentes. En el caso anterior se utilizó `else if` en lugar de sólo `if`. En segundo lugar, el orden de las sentencias tiene un impacto importante. Puede probar el resultado de lo anterior ejecutando el código que se encuentra a continuación.

```python
for number in range(1, 41):
    if number % 3 == 0 and number % 5 == 0:
        print("FizzBuzz")
    elif number % 3 == 0:
        print("Fizz")
    elif number % 5 == 0:
        print("buzz")
    else:
        print(number)
```

## **Conclusión**
---
En esta lectura, ha aprendido por qué debe utilizar el pseudocódigo, cuándo debe utilizarse y cómo escribir pseudocódigo.

El alcance del pseudocódigo va más allá de su cometido de comprender un nuevo lenguaje de programación. Es una práctica valiosa que ayuda a visualizar el flujo del código. Esboza qué habilidades o bibliotecas pueden ser necesarias para completar una tarea.

Los ingenieros de software lo utilizan al principio de su andadura para hacerse una idea de cómo podría fluir un programa. Los ingenieros senior lo utilizan para demostrar ideas a un equipo. No hay una única forma de escribirlo, pero el estilo por el que se decida se parecerá a la estructura del lenguaje de programación que más le guste.