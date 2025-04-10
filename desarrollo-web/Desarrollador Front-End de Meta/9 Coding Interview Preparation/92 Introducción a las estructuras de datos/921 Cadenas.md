---
Fecha: 2024-12-25
Categoría: Estructuras de datos básicas
tags:
  - front-end
  - curso-9
  - modulo-2
---
Las cadenas son una característica de todos los lenguajes de programación. Una cadena puede definirse como una ==secuencia ordenada de caracteres o símbolos encerrados entre comillas simples o dobles coincidentes==. La mayoría de los lenguajes admiten tanto caracteres ASCII primarios como representaciones Unicode. **Un carácter ocupará un byte de memoria**. Sin embargo, existen muchas formas adicionales de representar cadenas.

En esta lectura, aprenderá sobre la estructura de datos string , cómo se representan las cadenas en los distintos lenguajes, para qué se utilizan habitualmente y por qué los lenguajes de programación hacen que las cadenas sean inmutables.

## **1 Representación de cadenas**
---
Existen diferencias críticas en la forma en que cada lenguaje representa y admite las cadenas. Todos los lenguajes admiten las operaciones básicas de crear, modificar, copiar y asignar cadenas a variables. Además, las acciones cotidianas incluyen **concatenar**, **añadir** cadenas, **encontrar la subcadena** y tratar con **colecciones de cadenas**.

Al procesar cadenas, muchos lenguajes le permitirán realizar acciones algebraicas sobre ellas. Por ejemplo, `String_A == String_B`, que devolverá un `true` o un `false` o `String_A < String_B` que determina cuál es alfabéticamente el primero. Algunos lenguajes permiten representar variables en una cadena pero requieren un símbolo especial. A menudo se trata de un signo de dólar `$` delante del nombre de la variable, pero en algunos casos también puede incluirse entre llaves `{}`. Las **banderas de escape** permiten incluir símbolos en una cadena. Imagine que desea incluir comillas dentro de una cadena.

`String = “the man said \”two more pints please\” to the barman”`

En este caso, el uso de la barra invertida `\` garantiza que la cadena conservará las comillas en la frase. Otros símbolos de escape podrían ser `#`, `%`,' o una comilla doble dentro de una cadena denotada por comillas simples. Aunque la implementación real puede diferir, el enfoque general para tratar con cadenas es el mismo.

## **2 Uso común**
---
Un área que trata mucho con cadenas es el ==Procesamiento del Lenguaje Natural (PLN)==. La forma en que se codifican las cadenas al leerlas desde diversos lugares como Twitter, archivos PDF, documentos de texto o Reddit puede plantear problemas inesperados. Éstos pueden crear complejos problemas de depuración si la aplicación procesa una representación de símbolos inusual que afecte a los resultados.

Al escribir cadenas en un programa, es habitual aplicar la ***tokenización***. Esto consiste en convertir una cadena en una matriz de cadenas más pequeñas. Aquí se identificaría un delimitador y se rompería la cadena en segmentos separados por dicho delimitador. Así, un párrafo podría dividirse en frases mediante el uso del punto (`.`) o una frase en palabras individuales mediante la segmentación por espacios (`" "`). Sin embargo, hay que tener cuidado al tokenizar el texto. Considere el texto siguiente que tiene tres símbolos de punto (`.`).

_A las 3.30 fui a la tienda y me gasté 40.40 dólares._

Convencionalmente, se leería como una sola frase, pero los puntos utilizados para indicar la hora y la cantidad de dinero son delimitadores, por lo que la frase se divide en tres partes.

La tokenización en datos procesados y formateados ofrece menos dificultades. Una forma habitual de almacenar representaciones de cadenas formateadas es mediante **valores separados por comas** (CSV) o **valores separados por tabulaciones** (TSV).

El procesamiento de este tipo de cadenas se conoce como _análisis sintáctico_, y la matriz devuelta será igual al tamaño del número de delimitadores encontrados, con el delimitador eliminado. He aquí un ejemplo de un archivo CSV que contiene las columnas de edad, nombre y color de pelo. Observe que no hay ninguna coma al final. A menos que se indique lo contrario, el símbolo de nueva línea también funciona como delimitador.

```
age,name,hair color
24,John,black
25,Tony,brown
34,Brian,blue
29,Mary,red
43,Martin,yellow
```

## **3 Inmutabilidad**
---
Un concepto importante a tener en cuenta al tratar con cadenas es si la cadena es mutable o inmutable. La mutabilidad se refiere a la ==capacidad de modificar una cadena después de haberla creado====. Algunos lenguajes como Ruby y PHP permiten modificar las cadenas después de su creación. Sin embargo, es más común utilizar la inmutabilidad, como en Java, C#, JavaScript, Python y Go.

Hay varias razones por las que los lenguajes de programación hacen inmutables las cadenas. Por un lado, puede reducir el consumo de memoria. En lugar de crear una variable que contenga una cadena, se diseña una reserva de cadenas para representar todas las cadenas utilizadas. El enfoque inmutable reutiliza la asignación de memoria haciendo que todas las instancias de string apunten a una única ubicación. Así, cuando se produce un cambio con una cadena, digamos que se convierte en strings, en lugar de cambiar el valor de string, se apunta la variable a otra instancia de strings. O se apunta a otro ejemplo inmutable que represente a strings, que se añade entonces a la reserva de cadenas.

Esto supone un gran ahorro de memoria. Considere la posibilidad de leer las palabras existentes en lugar de crear una posición de memoria para cada palabra, incluidas las que se repiten. El uso de un conjunto único reduce el espacio necesario. El inconveniente es que si su aplicación cambia constantemente los textos, se incurre en una penalización de memoria por cada alteración realizada.

## **Conclusión**
---
En esta lectura, ha aprendido sobre la estructura de datos de las cadenas, cómo se representan las cadenas en los distintos lenguajes, para qué se utilizan habitualmente y por qué los lenguajes de programación hacen que las cadenas sean inmutables.