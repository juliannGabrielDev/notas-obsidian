---
Fecha: 2024-12-26
Categoría: Estructuras de datos avanzadas
tags:
  - front-end
  - curso-9
  - modulo-2
---
- [[#1 ¿Qué es una hashtable?|1 ¿Qué es una hashtable?]]
- [[#2 Implementación de hashtables en Kotlin|2 Implementación de hashtables en Kotlin]]
- [[#3 ¿Qué es thread-safe y cómo se aplica a las hashtables?|3 ¿Qué es thread-safe y cómo se aplica a las hashtables?]]
- [[#4 ¿Cómo se relaciona la seguridad de hilos con la implementación de hashtables en Kotlin?|4 ¿Cómo se relaciona la seguridad de hilos con la implementación de hashtables en Kotlin?]]
- [[#5 Implementación de hashtable en Python|5 Implementación de hashtable en Python]]
- [[#Conclusión|Conclusión]]

Las clases de colección son clases especializadas para el almacenamiento y la recuperación de datos. En función de las necesidades de su aplicación, la selección de una estructura de datos adecuada puede influir significativamente en su enfoque de la codificación y en la eficacia de la aplicación. ==Una tabla hash almacena pares clave-valor y ofrece una búsqueda rápida==. Algunos lenguajes incluyen implementaciones listas para usar, mientras que otros requieren otro tipo de colección para actuar como una hashtable.

## 1 ¿Qué es una hashtable?
---
Una hashtable ofrece búsquedas muy rápidas para una aplicación. Esto se consigue creando una función hash que creará una salida alfanumérica (letras y números) a partir de una entrada dada. Este hash se utiliza entonces para determinar en qué lugar de la memoria hay que almacenar algo. Esto significa que ==cuando quiera saber si un elemento está en la estructura de datos, en lugar de buscar en cada elemento y hacer una comparación, sólo tiene que aplicar la función hashing y ver si ese elemento ha sido hasheado en la memoria==. Si tenemos en cuenta que una fuente de datos puede tener millones de entradas, no tener que comprobar cada una de ellas supone un gran ahorro de tiempo. Además, **es importante asegurarse de que la tabla hash no permita que se añadan nulos como claves o valores**. Esto puede causar un problema a la hora de comparar valores dentro de la tabla.

Ninguno de los lenguajes cubiertos en este curso tiene una implementación de hashtable incorporada. Así que, para implementar una instancia, es necesario alterar una estructura de datos existente para realizar las operaciones de una hashtable.

## 2 Implementación de hashtables en Kotlin
---
Mientras que Kotlin no tiene una implementación incorporada de una hashtable, se admite una estructura de datos muy similar llamada hashmap. Los hashmaps son muy similares a las hashtables ya que también almacenan pares clave-valor y utilizan un hash para determinar en qué parte de la memoria encontrar la clave. Hay algunas diferencias claras que deben tenerse en cuenta: un hashmap permitirá el uso de nulos para claves y valores, y no es thread-safe.

## 3 ¿Qué es thread-safe y cómo se aplica a las hashtables?
---
Los hilos ==son procesos que puede ejecutar un ordenador==. Normalmente, cuando enciende su ordenador, se inician una serie de procesos. Estos procesos incluyen cosas como iniciar un documento de Word, Excel, una aplicación Java, etc. Estos procesos suelen ejecutarse al mismo tiempo. ==Para ello, el compilador creará muchos hilos que pueden ejecutar el código. Así pues, un hilo es un pequeño trozo de código ejecutable que puede ejecutar un proceso==. Entonces, ¿cómo se puede decir que el código es thread-safe? ***Thread-safe*** significa que si va a escribir un programa que accede a una estructura de datos, puede duplicar esta aplicación y acceder a la misma estructura de datos a través de diferentes hilos sin causar un error. Tener cinco hilos diferentes trabajando en la misma estructura de datos puede hacer que su código se ejecute cinco veces más rápido, pero sólo es útil si la información que se está modificando se hace correctamente.

## 4 ¿Cómo se relaciona la seguridad de hilos con la implementación de hashtables en Kotlin?
---
Una característica de las hashtables es que **pueden sincronizarse**. ==Esto significa que si cinco procesos diferentes están utilizando y cambiando la misma información en una tabla, la información siempre será correcta==. Kotlin no proporciona una implementación de hashtables; sin embargo, existe una estructura de datos muy relacionable que puede adaptarse para este propósito llamada hashmaps. Los hashmaps tienen la misma implementación de clave, valor y búsqueda hash, pero no son seguros para los hilos. Por lo tanto, al implementar una hashtable en Kotlin, se puede tomar un hashmap y añadir algo de código que asegure la sincronización para que varios hilos puedan acceder a ella al mismo tiempo.

## 5 Implementación de hashtable en Python
---
Al igual que Kotlin, Python no tiene una implementación nativa de una hashtable. En la sección anterior, se demostró que se podía imitar una tabla utilizando una estructura existente llamada hashmap. Esto también puede hacerse en Python, aunque la estructura subyacente utilizada es un diccionario. ==Un diccionario es una estructura de datos apropiada para utilizar, ya que funciona según el mismo principio que una hashtable. A saber, almacena pares clave-valor==. Las claves son hashables y se utilizan como indicador del lugar de la memoria donde almacenar el valor. Esto significa que dispone de métodos de búsqueda e inserción muy rápidos. Además, los diccionarios ya son seguros para los hilos, por lo que no es necesario cambiarlos si necesita que las operaciones se realicen de forma concurrente.

## Conclusión
---
En esta lectura se ha hablado de las hashtables. La implementación de una hashtable depende del lenguaje. Aquí se demostró cómo un hashmap en Kotlin y un diccionario en Python son estructuras suficientemente similares a partir de las cuales se puede crear una hashtable.