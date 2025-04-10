---
Fecha: 2024-12-25
Categoría: Estructuras de datos de recogida
tags:
  - front-end
  - curso-9
  - modulo-2
---
- [[#1 Mutabilidad|1 Mutabilidad]]
- [[#2 ¿Por qué los conjuntos son tan rápidos?|2 ¿Por qué los conjuntos son tan rápidos?]]
- [[#3 Listas|3 Listas]]
- [[#Conclusión|Conclusión]]

Los conjuntos y las listas son tipos incorporados en muchos lenguajes con un tema general común a la mayoría. En la implementación real, existen algunas diferencias sutiles.

En esta lectura, explorará algunas de las diferencias entre listas y conjuntos en distintos lenguajes de programación.

## 1 Mutabilidad
---
Ya se ha hablado del concepto de **inmutabilidad**. Concretamente, se trata de cómo se crea una estructura de datos. Los objetos inmutables no pueden modificarse cuando se crean, mientras que los mutables pueden modificarse después de su creación. ==Los conjuntos son un ejemplo de estructura inmutable en la mayoría de los lenguajes de programación==. Sin embargo, los objetos que se añaden a los conjuntos pueden tratarse de forma diferente según el lenguaje. En JavaScript, puede añadir objetos mutables a un conjunto, lo que no está permitido en Python. Comprender esta diferencia fundamental le dará una idea de cómo utiliza el lenguaje los conjuntos.

## 2 ¿Por qué los conjuntos son tan rápidos?
---
La razón de la velocidad a la que los conjuntos pueden encontrar un elemento se debe a su **arquitectura subyacente**. ==Los conjuntos almacenan valores utilizando un enfoque hash==. Hacer hash de algo es tomarlo y generar un resultado único a partir de él. Esto se hace aplicándole un algoritmo que convierte la entrada en una salida alfanumérica simple (palabras y letras). Cada vez que el algoritmo vea la entrada, generará siempre la misma salida alfanumérica. Ésta se utiliza después en una tabla hash, que utiliza el hash único para informar de dónde almacenar un elemento en la memoria. Así, es posible saber con un solo cálculo si el valor está en la memoria o no. En lugar de buscar cada elemento de la lista, basta con aplicar la función hash y comprobar si se está utilizando.

Por lo tanto, los conjuntos son rápidos, ==pero la razón por la que son tan rápidos es también por la que no se puede cambiar el valor almacenado==. Si crea un hash para un elemento y lo almacena según ese hash, entonces cambia el elemento y el hash ya no podrá encontrarlo. Esta es una de las razones por las que Python sólo le permite almacenar objetos inmutables que no pueden cambiarse en conjuntos. No todos los lenguajes ofrecen esta protección. Por ejemplo, JavaScript sí permite almacenar objetos mutables. Por lo tanto, la protección del objeto se deja en manos del usuario cuando se codifica con conjuntos de JavaScript. ==Supongamos que desea alterar un valor mutable en JavaScript. En ese caso, es aconsejable extraer y borrar el objeto mutable antes de reinsertarlo en el conjunto como un nuevo elemento==.

Al igual que Python, Kotlin no permite alterar los elementos una vez que se han añadido a un conjunto. Esto significa que existe un acceso de sólo lectura al conjunto. Si desea conjuntos que puedan ser alterados, entonces Kotlin tiene otro tipo de conjunto llamado `MutableSet`. Los conjuntos en Kotlin son muy versátiles y ofrecen una serie de métodos incorporados como `max`, `min`, `sum` y `average`. Esto los hace muy prácticos a la hora de buscar elementos específicos dentro de un grupo de números.

## 3 Listas
---
Otro tipo de colección importante que conviene conocer son las listas. ==Las listas almacenan elementos en un orden determinado al que se puede acceder utilizando un índice==. Un índice no es más que un número que se pasa a la lista y que indica que debe devolverse el elemento que se encuentre en esa posición numérica. El índice es la forma en que se buscan los elementos en una lista. ==Si alguien quiere saber si algo está en una lista, tendría que hacer una búsqueda y comprobar cada elemento, por lo que son más lentas que un conjunto==. Además, una lista permite almacenar en ella todo tipo de elementos. No se distingue si un elemento es mutable o inmutable. Las listas también le permitirán almacenar duplicados de elementos. Existen distintos tipos de listas que se implementan de forma diferente.

Sin embargo, el punto fundamental que merece la pena recordar es que una lista le permite almacenar elementos que se repiten y elementos de distintos tipos. Una lista está ordenada, lo que significa que conservará el orden de los elementos a medida que se vayan insertando. Esto es diferente de los conjuntos, que pueden almacenar los elementos en lugares distintos de donde se introdujeron inicialmente.

Conocer estas sutiles diferencias puede ser útil a la hora de decidir qué tipo de estructura de datos desea seleccionar. Tanto los conjuntos como las listas son útiles, pero como actúan de forma diferente, serán más útiles en unas situaciones que en otras. Asegurarse de que una lista o un conjunto es lo más adecuado en una situación es el truco.

## Conclusión
---
En esta lectura se ha ofrecido una breve visión general sobre las listas y los conjuntos en diferentes lenguas. Se han comentado los puntos fuertes y débiles de ambas, así como algunas ideas interesantes sobre su funcionamiento. Con suerte, ¡pensará en ellos la próxima vez que planee almacenar datos!