---
Fecha: 2024-12-25
Categoría: Introducción a la informática
tags:
  - front-end
  - curso-9
  - modulo-1
---
## **Introducción**
---
De todos es sabido que los ordenadores piensan en ceros y unos. Pero, cómo funciona esto en la práctica es un poco más complejo de lo que uno podría pensar inicialmente. Anteriormente exploró cómo los ordenadores utilizan datos binarios para almacenar y procesar información. En esta lectura, aprenderá más sobre el binario, incluyendo cómo trabajar con la lógica booleana, las tablas de verdad y las puertas.

Puede que piense que utilizar sólo dos entradas es restrictivo. Sin embargo, es extraordinariamente versátil y ofrece una amplia gama de opciones si se combina con el álgebra booleana y los circuitos.

## **1 Lógica booleana**
---
Una función booleana asigna dos entradas a un valor. Estas entradas están limitadas a dos estados. Estos estados pueden considerarse: **encendido/apagado**, **verdadero/falso** o **1/0**. Para definir una función booleana, sólo necesita especificar la salida de su inclusión. He aquí un ejemplo de 4 funciones:

![Los conjuntos y las listas son tipos incorporados en muchos lenguajes con un tema general común a la mayoría. En la implementa](logica-booleana.webp)

NOT toma un valor **x** y lo resuelve en un **0** o un **1**. OR toma dos argumentos **(x, y)** para generar una salida de **1**. Sólo uno de los valores **x** o **y** debe ser **1**. Si ambos valores son **0**, la salida es **0**. AND requiere que ambas entradas sean **1** antes de poder generar un **1**. Por último, XOR tomará dos valores cualesquiera y determinará si son iguales; si es así, la salida es **1**. En todos los demás casos, el resultado es **0**.

![Expresiones booleanas con sus símbolos computacionales.](simbolos-computacionales.webp)

Los mismos conceptos pueden representarse computacionalmente. En esta tabla, las expresiones booleanas están a la izquierda y sus símbolos computacionales a la derecha. Lo más habitual es que se combinen con sentencias condicionales o iteradores. Así, podría esperar un código parecido al siguiente fragmento de código:

```java
Boolean x = false;
do {
	System.out.println("executed repeatedly");
} While(!x);
```

En el código anterior, se ha establecido un booleano en false. A continuación, un bucle do/while ejecuta continuamente el código que se encuentra dentro del do hasta que el valor para **x** cambia a true. Generalmente, usted estaría buscando un resultado específico, y el uso de la lógica booleana le permite seguir buscando hasta que el resultado se convierte en true. Observe cómo se aplica la función NOT en el bucle while para comprobar si debe existir otra iteración.

## **2 Tablas de verdad**
---
Dado el número finito de salidas de las funciones booleanas, es posible representar todas las permutaciones en una tabla.

![[tablas-verdad.webp]]

Esta imagen muestra todas las permutaciones para cada una de las funciones booleanas. Las columnas **X** e **Y** indican si recibe un **0** o un **1**, y la **XY** indica el resultado final. La función NOT sólo tiene una salida y una entrada, por lo que la tabla es sólo **de 2 x 2**. En comparación, los otros tres ejemplos toman todos dos entradas y generan un único resultado.

## **3 Compuertas**
---
El bloque de construcción fundamental de los circuitos lógicos digitales es la puerta. Las funciones lógicas se implementan a través de su interconexión. Una puerta es un circuito electrónico que genera una salida booleana a partir de sus entradas.

![Y, O, No y Xor y sus símbolos gráficos, Función algebraica y tabla de verdad](compuertas.webp)

En la imagen anterior se ilustran las cuatro funciones booleanas básicas. El símbolo gráfico es la forma en que estas puertas se representan en los diagramas. A menudo se encontrará con diagramas de circuitos que albergan una serie de compuertas interconectadas. La función Algebraica demuestra cómo se describen estas compuertas cuando se escriben como fórmulas.

Por último, las tablas de verdad esbozan los resultados de una entrada dada a la compuerta. En un nivel primitivo, cada entrada denotada por **A y** **B** representa una corriente que puede pasar por el circuito. Estas entradas pueden estar conectadas a un interruptor, o a un botón, que puede activarse haciendo que se transmita un **0** o un **1**. La expresión de esta lógica booleana se construye cuando las puertas del circuito se combinan para formar circuitos complejos. La salida final **Q** se determina a partir de las maquinaciones realizadas en las entradas **A**, **B** y **C**.

![Diagrama que representa las entradas A, B y C, los circuitos complejos y la salida final Q](circuitos-complejos.webp)

## **Conclusión**
---
Esta lectura demuestra cómo un simple **0** y **1** pueden combinarse y amplificarse mediante la lógica booleana, las tablas de la verdad y las puertas lógicas para generar salidas más complejas. Ha aprendido más sobre el binario, incluyendo cómo trabajar con la lógica booleana, las tablas de verdad y las puertas.