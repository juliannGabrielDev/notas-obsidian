---
Fecha: 2024-12-25
Categoría: Estructuras de datos básicas
tags:
  - front-end
  - curso-9
  - modulo-2
---
- [[#**Introducción**|Introducción]]
- [[#**1 Definición**|1 Definición]]
- [[#**2 Ejemplo**|2 Ejemplo]]
- [[#**Conclusión**|Conclusión]]

## Introducción
---
En esta lectura se hablará de los objetos. Los objetos son los bloques de construcción de todo código y desempeñan un papel especialmente importante en la programación orientada a objetos (POO). En esta lectura, se expondrán las ventajas de utilizar objetos, así como cierta terminología importante relacionada con el uso de objetos.

## 1 Definición
---
Un objeto es un concepto de programación que significa que una estructura tiene tanto **estado** como **comportamiento**. ==En este caso, el comportamiento se refiere a la capacidad del objeto para realizar alguna acción==. A medida que avance en este curso, será testigo de muchos casos de objetos que exhiben diferentes comportamientos. Concretamente, se refiere a llamar a los métodos de un objeto. Un ejemplo de ello podría ser llamar al método de ordenación de un array. Esto tiene como resultado la reorganización de los elementos de un array para que estén organizados en relación unos con otros.

==El **estado** se refiere a la información sobre un objeto==. Otra palabra para esto con la que puede estar familiarizado es atributos de objeto. Si crea una clase persona y la instancia a un objeto, un ejemplo de un estado podría ser la edad o el nombre de la persona. ==El comportamiento entonces podría referirse a una acción que se requiere de esta persona-objeto, como correr o placar==.

Las clases se describen comúnmente como planos de un objeto. Por extensión, un objeto puede describirse como una instancia de una clase. El uso más común de los objetos es en la programación orientada a objetos, donde el código se encapsula en objetos, y estos objetos luego interactúan entre sí.

## 2 Ejemplo
---
Uno de los puntos fuertes considerables de utilizar objetos para instanciar una clase es que sólo necesita crear una plantilla para saber cómo actuará un objeto. A continuación, tendrá libertad para crear múltiples instancias de esta clase que puedan interactuar entre sí. Considere un equipo de fútbol con 11 jugadores. Sólo es necesario esbozar una clase que pueda contener distintas características de velocidad, agilidad y ritmo de trabajo. Esto puede reducir seriamente la sobrecarga de código en la creación de un partido de fútbol. Características como la velocidad y la agilidad se conocen como variables de instancia y puede decirse que están relacionadas con el estado del objeto. Ninguna unidad ajena al objeto compartirá esta instancia. Dos jugadores pueden tener una instancia de aptitud física. Cambiarla en uno no afectará a la instancia de aptitud física que se encuentre en los otros objetos. Puede cambiar las instancias de una clase a través del constructor o de un método interno del objeto. En Java, una instanciación típica de una clase es la siguiente:

`Player player1 = new Player(agility = 54, speed = 88, fitness = 90);`

`Player player2 = new Player(agility = 90, speed = 64, fitness = 83);`

En este ejemplo, la clase jugador crea dos objetos, `player1` y `player2`. Las variables dentro de la clase se establecen de forma diferente en función de los valores que se encuentran dentro de los corchetes. También es necesario que exista un método para modificar la variable. En el transcurso de un partido, un jugador puede cansarse. Se puede llamar a un método para reducir la instancia de la variable para reflejar esto.

`player1.set_fitness(80)`

Esto alterará el nivel de forma física de `player1` pero no afectará a los demás jugadores. Los métodos utilizados para modificar las instancias de los atributos se denominan generalmente `getters` y `setters`.

Un mayor control de los objetos está disponible a través de los otros métodos que se encuentran con el objeto. Un comando como

`player1.kick()`

haría que el objeto asignado a `player1` ejecutara el procedimiento de patear el balón.

La clase jugador permite crear un equipo con distintas habilidades que pueden jugar. Otro concepto relacionado con el uso de objetos es la herencia. Imagine que necesita crear otro ser humano en el terreno de juego, como un árbitro, que no juegue pero que realice acciones relacionadas con el juego, como correr y su aspecto general. Es posible que desee reutilizar parte del código que se encuentra en el jugador sin crear un jugador. Aquí crearía una clase que contenga todos los atributos comunes que desee conservar, y cada objeto puede heredarlos, como se muestra.

![[herencia.canvas]]

Así, los métodos estándar como correr, cansarse y seguir la pelota pueden encontrarse todos dentro de `Humans`, pero puede diferenciarse cómo se relacionan con la clase `player` y la clase `referee`. Esta noción de tener un concepto general(human) que puede manifestarse en diferentes formas (jugadores, directivos, árbitros) se conoce como polimorfismo. Una forma, muchas formas. El ejemplo clásico es el uso de formas. Una forma general contendrá los conceptos de área, diámetro y altura. Luego, cada instancia de forma (cuadrado, triángulo, círculo) aplicará las implementaciones reales de cómo se ven estos atributos en su estado dado.

## Conclusión
---
En esta lectura se ha explorado el concepto de objeto, con especial atención a su utilidad cuando se utiliza en un enfoque de programación orientada a objetos.