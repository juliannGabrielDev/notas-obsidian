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
La informática consiste en resolver problemas. La invención del ordenador nos ha proporcionado una capacidad sin precedentes para conceptualizar y superar problemas, reales e imaginarios. Antes, había que lanzar un avión desde el cielo para comprobar si volaría. O recopilar datos meteorológicos y hacer predicciones basadas en patrones. Ahora es posible modelar escenarios de forma realista y crear una solución virtualmente antes de enviar un globo meteorológico o atar siquiera un ala a un avión. Esta lectura trata de cómo definir soluciones a enunciados de problemas articulando el problema, formulando un modelo y afinando la solución.

## **1 Planteamiento del problema**
---
El primer paso para resolver un problema es articularlo. Necesito conseguir A, con herramientas T, dadas unas restricciones C. A modo de concreción de la noción de buenas prácticas a la hora de abordar el diseño de una solución, consideremos un problema del mundo real. Supongamos que tiene que diseñar una aplicación que entretenga a un niño jugando a las adivinanzas. A primera vista, parece una tarea sencilla: ordenador + juego = niño feliz. Pero, antes de empezar, merece la pena determinar algunos detalles.

1. ¿Cómo interactuará el niño con el ordenador?

2. ¿Qué nivel de preguntas debe formular?
  
3. ¿Desde dónde se generarán estas preguntas?
  
4. ¿Cómo se almacenarán?
  
5. ¿Cómo se comprobarán las respuestas?
  
6. ¿Cómo se iniciará y finalizará el programa?

En este escenario, las cuestiones están relacionadas tanto con el hardware como con el software. En primer lugar, ¿tiene el niño una edad en la que no se requieren medidas de seguridad? En otras palabras, es importante que la solución ideal se contemple teniendo en cuenta cómo se va a utilizar la aplicación final. Regalar a un niño pequeño un portátil caro puede comprarle una mañana de paz, ¡pero luego puede costarle el sueldo de un mes! Este mismo pensamiento debe extenderse a la aplicación que se visualiza. ¿Podrá el jugador interactuar con su aplicación con una señal de Internet potente? ¿Existen otras limitaciones como que la salida tenga que ser compatible con distintos tipos de teléfonos móviles? ¿Hay algún sistema operativo o navegador específico que deba ser atendido? Todas estas son cuestiones que debe tener en cuenta antes de empezar a crear la aplicación.

## **2 Formular un modelo**
---
Ahora que se tiene una idea de algunas de las limitaciones del proyecto, se pueden proponer posibles soluciones. Imaginemos que el niño está en edad de utilizar un ordenador, que la aplicación sólo tiene que ejecutarse en un portátil, que todo el almacenamiento se hará localmente (para que no haya problemas de conectividad a Internet) y que la introducción de datos puede hacerse utilizando un teclado en la línea de comandos. Estupendo, ahora es posible profundizar en el proyecto.

Una vez establecido el alcance del proyecto, es hora de considerar qué es lo que el ordenador debe hacer. Un algoritmo puede definirse como una secuencia precisa de instrucciones para resolver un problema. Puede ser útil generalizar primero el problema y luego esbozar con más precisión la secuencia de instrucciones necesarias antes de codificar una implantación. Esto es como adoptar un enfoque algorítmico para resolver el problema. A menudo, un programador obtendrá una intuición sobre cómo debería ser la solución esbozando primero el problema mediante pseudocódigo. Puede tratarse de una descripción basada en texto que detalle los requisitos.

```
Generate a question
Take n user input
Compare input with answer
Return a result.
```

Trazar los pasos en una lista es un buen primer paso. Ahora, se puede considerar cómo generar una pregunta que sea apropiada para la edad. Generar preguntas dinámicamente a partir de una enciclopedia en línea o de alguna otra fuente en línea podría llevar mucho tiempo. Como alternativa, podría identificar una fuente de preguntas y respuestas ya compiladas.

En segundo lugar, ¿cómo se toma la entrada del usuario? Se ha establecido que el teclado es viable, pero ¿hasta qué punto es capaz el niño de teclear? Comparar una solución con texto ofrece sus propios retos. ¿Tendría que ser una coincidencia directa, habría que tener en cuenta la ortografía, la puntuación y las mayúsculas? Potencialmente, las preguntas podrían ser de opción múltiple. Tomar conciencia de todas estas consideraciones es el objetivo de esbozar claramente el planteamiento del problema en lugar de lanzarse a buscar una solución.

## **3 Afinar la solución**
---
Reflexionando, usted determina que un planteamiento de conocimiento trivial ofrecerá demasiados obstáculos, por lo que el proyecto se define más como un juego de adivinanzas numéricas. Es apropiado para todas las edades y no hay necesidad de utilizar fuentes externas. Y debería poder implementarse con la mayoría de los lenguajes de programación.

```
Generate a random number
Take in user input store in a variable
Compare input with answer
Return a result
```

Una vez esbozados los requisitos generales, es posible completar los puntos más finos. A continuación se muestra un diagrama de flujo del pseudocódigo y puede dar más ideas sobre cómo enmarcar mejor la solución.

![Diagrama de flujo de pseudocódigo que da una idea de cómo enmarcar la solución](diagrama-flujo.webp)

El examen del diagrama de flujo permite identificar otras consideraciones. ¿Se ejecutará el programa una sola vez? ¿Qué se puede añadir para mejorar la experiencia del usuario? Imprimir un mensaje de fallo puede no ser un gran resultado. En su lugar, una opción podría ser ofrecer otra oportunidad de adivinar. Otras consideraciones podrían ser proporcionar indicaciones que pudieran utilizarse para dirigir al usuario hacia la respuesta correcta. Y, debería decidir qué ocurre si el usuario introduce un número distinto de un número en el programa.

![Diagrama de flujo de pseudocódigo que esboza los posibles resultados de un acierto y un error.](diagrama-flujo-2.webp)

Ahora que se han esbozado las distintas condiciones, es posible elegir un lenguaje e implementar una solución. Al adoptar un enfoque sistemático para la resolución de problemas, habrá identificado algunos problemas potenciales antes de iniciar el proyecto y podrá añadir algunas correcciones de rumbo. Tras evaluar la solución, el proyecto podría ahora cambiar de ámbito. En lugar de crear un juego para que un niño lo ponga en práctica, el programa podría en su lugar establecer un entorno para que el niño pueda crear el juego por sí mismo, utilizando las descripciones claras como guía.

## **4 Conclusión**
---
Los ordenadores son una excelente forma de modelar programas y un medio para poner en práctica una solución. Es responsabilidad del programador emplear un enfoque sistemático en el desarrollo de soluciones. El mismo procedimiento utilizado para identificar un buen proyecto para un niño puede aplicarse a la creación de una aplicación para el trabajo. Es imperativo establecer estos buenos hábitos de trabajo al principio de su carrera y mantenerlos a medida que progrese su dominio de la codificación.