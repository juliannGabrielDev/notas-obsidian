---
Fecha: 2024-12-25
Categoría: Estructuras de datos básicas
tags:
  - front-end
  - curso-9
  - modulo-2
---
Un número entero se utiliza para contener valores numéricos. Un entero puede ser con signo (contiene tanto números positivos como negativos), o sin signo (sólo contendrá números positivos). Los enteros se representan en binario y una representación esencial necesitará **4 bytes**.

En esta lectura, aprenderá sobre la estructura de datos de los enteros, por ejemplo, cómo se representan los enteros, la asignación de memoria para los enteros y la clase envolvente de enteros en Java.

## **1 Representación de enteros**
---
Hay varias formas de representar enteros en binario. Un ejemplo típico es el **signo-magnitud**. Si los enteros se representan en binario, ¿cómo pueden distinguir entre un valor positivo y uno negativo? Signo-magnitud propone utilizar un indicador en el extremo izquierdo del número binario para denotar la polaridad.

|Entero|Representación signo-magnitud|
|---|---|
|2|0010|
|1|0001|
|+0|0000|
|-0|1000|
|-1|1001|
|-2|1010|

Un número entero no puede representar fracciones. Para ello, se utilizaría el decimal o el flotante. Para representar números enteros se utiliza un número fijo de bytes, cuyo tamaño puede especificarse en algunos lenguajes. Existe un enfoque estandarizado para representar números denominado norma IEEE 754, que esboza un conjunto común de normas para representar todos los números.

Algunos lenguajes de alto nivel como Python y JavaScript suscriben este enfoque y encapsulan la inicialización de los números enteros en esta representación fija. Esto facilita el trabajo con números en estos lenguajes dinámicos de alto nivel, pero elimina la posibilidad de personalizar su enfoque para permitir la optimización de la memoria.

## **2 Asignación de memoria**
---
Otros lenguajes tipados estáticamente como C++, Rust, Ada y C le permiten personalizar el tamaño en memoria. C++ le permite personalizar su entero. Si utiliza `unsigned short int` sólo necesitará 2 bytes. Este ahorro puede acumularse si su aplicación incluye muchos números positivos que no requieren una precisión al grado de las fracciones.

Rust va un paso más allá y permite la instanciación de enteros sin signo de 1 byte. Este `int` limitado puede contener enteros de 0 - 255. Aunque puede no parecer un rango enorme con el que tratar, si está trabajando con píxeles, estaría trabajando con una tupla de valores en este rango. El procesamiento de imágenes es un proceso que consume mucha CPU y poder almacenar 8 píxeles por el precio estándar de 1 supone un ahorro enorme.

## **3 Clases envolventes**
---
Además de los enteros primitivos denotados por `int`, Java le permite envolver el valor de la primitiva en una clase envolvente `Integer`. Esto permite varios métodos para tratar con enteros, como la conversión de una cadena a un doble, comparaciones, tamaño máximo y mínimo, etc. La clase de enteros es inmutable, lo que la hace segura para los hilos. La funcionalidad y seguridad adicionales conllevan un coste de memoria, y el objeto `Integer` ocupará 16 bytes de memoria para almacenarse.

## **Conclusión**
---
Existe una enorme libertad a la hora de controlar cómo se almacenan sus cifras en la memoria. Mientras que un lenguaje de alto nivel tipado dinámicamente se pone en marcha, puede tener rendimientos limitados si su aplicación se vuelve pesada en cuanto a recursos. Supongamos que trabaja con Arduinos u otros aparatos electrónicos de aficionado. En ese caso, el espacio se convierte en una prima, y la libertad de personalización puede ser la diferencia entre una aplicación funcional y otra que no lo es. Sin embargo, si está desarrollando una aplicación que requiere cantidades sustanciales de memoria disponible, utilizar números enteros rápidamente y no tener que preocuparse por los detalles puede ser el camino a seguir.

En esta lectura, ha aprendido sobre la estructura de datos de enteros, por ejemplo, cómo se representan los enteros, la asignación de memoria para enteros y la clase envoltorio de enteros.