---
Fecha: 2024-12-25
Categoría: Estructuras de datos de recogida
tags:
  - front-end
  - curso-9
  - modulo-2
---
- [[#Introducción|Introducción]]
- [[#1 Pilas|1 Pilas]]
- [[#2 Colas|2 Colas]]
- [[#Conclusión|Conclusión]]

## Introducción
---
Una pila es una ==estructura de datos fundamental que limita la forma en que se almacenan los datos en una aplicación==. En concreto, los elementos deben adherirse a la política de entrada o salida de **último en entrar, primero en salir**. Diferentes lenguajes tienen diferentes implementaciones, aunque en conjunto, el resultado general es el mismo. Una cola es muy similar a una pila; sin embargo, el orden de entrada es diferente, favoreciendo una política de **primero en entrar, primero en salir**.

En esta lectura, conocerá algunas de las diferencias inherentes tanto a las pilas como a las colas en los distintos lenguajes de programación.

## 1 Pilas
---
Las pilas son un ejemplo de un tipo de datos abstracto. En informática, esto significa que hay algunas características muy importantes que deben cumplirse a la hora de implementarlo, pero no hay versiones reales incorporadas que pueda importar sin más. Para las pilas, el principio importante es **LIFO** o **último en entrar, primero en salir**. La analogía para las pilas puede ser visualizar una pila de platos en una tabla de lavar. A medida que se limpia cada plato, se coloca encima del anterior. Para secarlos, cada plato debe tomarse de la parte superior. Así, el último plato añadido a la pila se seca primero, y el primer plato de la pila se seca el último. Un uso común de las pilas es guardar el historial de su navegador. Cada vez que pulsa atrás, se carga la página visitada anteriormente y, a continuación, se lee en la pila.

Una implementación común de una pila en JavaScript es mediante el uso de una matriz y asegurándose de que actúa sólo de la manera en que actuaría una pila. Tomar una estructura de datos y utilizarla para construir otro tipo de estructura de datos se dice que es utilizar un adaptador contenedor. En este caso, el array es el contenedor, y la adaptación le obliga a comportarse como debería hacerlo una pila. Las características importantes de una pila son `push`, `pop`, `peek` y `count`. `Push` añade un elemento a la parte superior de la pila. Utilizar una matriz significa que el recuento debe saber siempre en qué parte de la matriz fue el último elemento. Igualmente, para el método `pop`, tener un recuento para la matriz es importante, ya que pop sólo devuelve el último elemento introducido en la pila.

## 2 Colas
---
Una cola, al igual que una pila, es una estructura de datos lineal que conserva el orden en que se introdujeron los elementos. ==Cuando se habla de una estructura lineal, significa que los elementos se almacenan en el orden en que se añadieron==. Al igual que una pila, la cola tiene una implementación estricta de cómo se añaden y eliminan los elementos. Mientras que una pila implementa un enfoque LIFO, las colas funcionan con un enfoque **FIFO** (**primero en entrar, primero en salir**). Así, el primer elemento que se añada a la cola será el primer elemento que se elimine. Al igual que un cliente que hace cola para realizar una compra, las colas buscan aplicar una política que dé importancia a la hora de llegada. Esto tiene algunos beneficios en el mundo real cuando se implementan cosas como la programación de la CPU y el disco, donde es importante ocuparse de las tareas a medida que llegan.

Una cola es un tipo de datos abstracto en Swift, lo que significa que para utilizar la funcionalidad de una cola, primero tendría que codificar una estructura que actuará de esa manera. Dos términos importantes asociados a las colas son `enqueue` (para añadir un elemento a la cola) y `dequeue` (para eliminar un elemento de la parte posterior de una lista). El enfoque más sencillo para crear una cola es utilizar una matriz como adaptador contenedor. Dado que una cola sólo saca elementos de la parte delantera de la cola, el tiempo de consulta será siempre `O(1)`, por lo que cualquier aplicación construida con este enfoque puede esperar un servicio muy rápido. Al igual que con las pilas, los métodos disponibles para una cola son mínimos, siendo los más importantes `pico`, `pop`, `push` y `tamaño`.

Python implementa varias clases de cola variantes que están todas sincronizadas. ==La sincronización es un concepto informático que significa que todos los accesos a los datos que se encuentran en ella se gestionan de forma que sólo pueda acceder a la estructura de datos un proceso a la vez==. Esto es importante cuando se piensa en la computación en nube y en tener muchas fuentes diferentes intentando buscar y cambiar datos al mismo tiempo. Además de FIFO y LIFO, la implementación de colas en Python incluye una cola de prioridad. ==Una cola de prioridad, como su nombre indica, consiste en asignar importancia a los elementos que se encuentran en la cola==. Así, en lugar de un orden de llegada, el servicio se basa en la importancia. Esto se parece un poco a la cola VIP del concierto.

## Conclusión
---
Seleccionar la estructura de datos adecuada para la tarea apropiada es una decisión de programación muy importante, ya que puede afectar a todo el proyecto. Usted seleccionaría una pila cuando exista la necesidad de mantener el orden en el que se introduce un elemento y de devolverlos de una forma muy específica. Una cola sirve para mantener el orden, pero se regirá por reglas diferentes a las de una pila. Por último, si desea una estructura de datos a la que pueda asignar importancia, entonces merece la pena considerar una cola de prioridad.