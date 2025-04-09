---
Fecha: 2024-12-25
Categoría: Estructuras de datos básicas
tags:
  - front-end
  - curso-9
  - modulo-2
---
Cuando ponga a prueba sus conocimientos en este curso, a menudo se le presentarán dos opciones: elección múltiple y verdadero o falso. Esta última es un ejemplo de booleano; una cosa es o no es. En esta lectura, aprenderá más sobre las estructuras de datos booleanas y las características fundamentales para trabajar con ellas, las sentencias condicionales y los operadores lógicos.

## **1 Expresiones condicionales**
---
Las expresiones booleanas pueden tomar una serie de operadores relacionales.

| Opador | Significado       |
| ------ | ----------------- |
| >      | Mayor que         |
| <      | Menor que         |
| >=     | Mayor o igual que |
| <=     | Menor o igual que |
| ==     | Igual a           |
| !=     | No igual a        |

Éstas le permiten interrogar algunos datos antes de ejecutar diferentes opciones de código. Por ello, las expresiones booleanas suelen denominarse condicionales. Combínelas con sentencias condicionales y tendrá una implementación temprana de la IA.

Las sentencias condicionales son: `if`, `else`, `else if`, `while` y así sucesivamente. Un bloque condicional puede permitirle ejecutar un conjunto de instrucciones en una condición y otro si las condiciones son diferentes. 

```python
if right > wrong:
    doTheRightThing()
elif wrong > right:
    doTheWrongThing()
else:
    keepResearching()
```

Utilizando expresiones booleanas como indicadores, puede utilizar operadores relacionales para determinar qué línea de código debe ejecutarse. En este ejemplo, tiene un ordenador evaluando entre correcto e incorrecto. Esto tiene múltiples aplicaciones y se utiliza habitualmente. Por último, si no ha cumplido ninguna de sus condiciones, puede emplear un bloque de código `catch-all`. Los roombas son un buen ejemplo de cómo puede utilizarse este código en la vida cotidiana. En lugar de correcto e incorrecto, dispondrá de sensores rudimentarios que determinan qué motores deben activarse en función de la distancia y el impacto.

## **2 Operadores lógicos**
---
Además, es posible que desee ampliar el alcance de su aplicación utilizando operadores lógicos.

| Operadores lógicos |            |
| ------------------ | ---------- |
| \|\|               | Lógico OR  |
| &&                 | Lógico AND |
| ¡!                 | Lógico NOT |

Estas expresiones lógicas pueden combinarse con expresiones booleanas para dar mayor diversidad a su código.

```python
if condition_1 || condition_2:
    doActionOne()
elif condition_1 && condition_2:
    doActionTwo()
elif !condition_1:
    doActionFour()
else:
    waitForInstruction()
```

En este código, se comprueban cuatro resultados. En primer lugar, tomemos `condition_1` o `condition_2`, y sigamos con el ejemplo de Roomba. Si la detección de proximidad o de impacto es verdadera, entonces la acción uno podría ser parar y dar marcha atrás. Si hay detección de proximidad e impacto, entonces activará una alarma. Si no hay detección de proximidad, seguirá enviando potencia a los motores de avance. Por último, si no se cumple ninguna condición, debe haber algún código a prueba de fallos listo para activarse.

El uso de la lógica booleana es la columna vertebral del diseño de circuitos. Es una forma de interpretar conjuntamente los operadores booleanos. Las formas del diagrama siguiente son compuertas que se activan cuando se disparan determinados operadores booleanos. Se envía una señal a través de los hilos (representados por las líneas de entrada y salida). El operador AND dice que si ambos hilos son verdaderos, entonces continúa esta línea de ejecución. Al mismo tiempo, el NAND especifica que sólo dos afirmaciones falsas desencadenarán una reacción.

![[and-or-not-nand.webp]]

Combinadas, pueden utilizarse para tomar decisiones complejas y hacer que un dispositivo funcione de diversas maneras, dependiendo de la entrada de los sensores.

![[diagrama-logico.webp]]

## **Conclusión**
---
Para concluir, las expresiones booleanas son verdaderas o falsas, y su equivalencia en binario sería `0` ó `1`. Al igual que con el binario, podría pensar que el hecho de tener sólo dos valores resulta en una capacidad limitada. Sin embargo, pueden alcanzar un nivel de complejidad sorprendentemente elevado cuando se combinan con otras construcciones matemáticas como las sentencias condicionales y los operadores lógicos. Los booleanos pueden utilizarse en sus programas informáticos para informar de qué operaciones deben ejecutarse de forma automatizada y forman la columna vertebral de los diagramas de circuitos.

En esta lectura, ha aprendido más sobre las estructuras de datos booleanas y las características críticas para trabajar con ellas, las sentencias condicionales y los operadores lógicos.