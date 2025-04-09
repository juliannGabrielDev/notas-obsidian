---
Fecha: 2024-12-17
Fuente: Coursera
Notas relacionadas:
  - "[[724 Importar módulos y bibliotecas en Python]]"
tags:
  - ciberseguridad
  - curso-7
  - modulo-3
---
Anteriormente se le presentaron las expresiones regulares y un par de símbolos que puede utilizar para construir patrones de expresiones regulares. En esta lectura, explorará otros símbolos de expresiones regulares que pueden utilizarse en un contexto de ciberseguridad. También aprenderá más sobre el módulo `re` y su función r`e.findall()`.
## Conceptos básicos de las expresiones regulares

Una **expresión regular (regex)** es una secuencia de caracteres que forma un patrón. Puede utilizarlas en Python para buscar una gran variedad de patrones. Por ejemplo, direcciones IP, correos electrónicos o ID de dispositivos.

Para acceder a las expresiones regulares y funciones relacionadas en Python, primero debe importar el módulo `re`. Debe utilizar la siguiente línea de código para importar el módulo `re`:

```python
import re
```

Las expresiones regulares se almacenan en Python como cadenas. Después, estas cadenas se utilizan en las funciones del módulo `re` para buscar en otras cadenas. Hay muchas funciones en el módulo `re`, pero explorará cómo funcionan las expresiones regulares a través de `re.findall()`. La función `re.findall()` devuelve una lista de coincidencias con una expresión regular. Requiere dos parámetros. El primero es la cadena que contiene el patrón de la expresión regular, y el segundo es la cadena en la que desea buscar.

Los patrones que componen una expresión regular están formados por caracteres alfanuméricos y símbolos especiales. Si un patrón de expresión regular consta sólo de caracteres alfanuméricos, Python revisará la cadena especificada en busca de coincidencias con este patrón y las devolverá. En el siguiente ejemplo, el primer parámetro es un patrón de expresión regular formado únicamente por los caracteres alfanuméricos `"ts"`. El segundo parámetro, `"tsnow, tshah, bmoreno"`, es la cadena en la que buscará. Puede ejecutar el siguiente código para explorar lo que devuelve:

```python
import re

re.findall("ts", "tsnow, tshah, bmoreno")
```

La salida es una lista de sólo dos elementos, las dos coincidencias con `"ts"`: `['ts', 'ts']`.

Si quiere hacer algo más que buscar cadenas específicas, debe incorporar símbolos especiales a sus expresiones regulares.
## Símbolos de expresión regular

### Símbolos para tipos de caracteres

Puede utilizar una gran variedad de símbolos para formar un patrón para su expresión regular. Algunos de estos símbolos identifican un tipo de carácter concreto. Por ejemplo, `\w` coincide con cualquier carácter alfanumérico.

**Nota:** El símbolo `\w` también coincide con el guión bajo ( `_` ).

Puede ejecutar este código para explorar lo que devuelve `re.findall()` al aplicar la expresión regular de `"\w"` al ID de dispositivo de `"h32rb17"`.

```python
import re

re.findall("\w", "h32rb17")
```

Dado que cada carácter de este ID de dispositivo es un carácter alfanumérico, Python devuelve una lista con siete elementos. Cada elemento representa uno de los caracteres del ID del dispositivo.

Puede utilizar estos símbolos adicionales para coincidir con tipos específicos de caracteres:

- `.` coincide con todos los caracteres, incluidos los símbolos

- `\d` coincide con todos los dígitos simples `[0-9]`

- `\s` coincide con todos los espacios simples

- `\.` coincide con el punto

El siguiente código busca en el mismo ID de dispositivo que el ejemplo anterior, pero cambia el patrón de la expresión regular a "\d". Cuando lo ejecute, le devolverá una lista diferente:

```python
import re

re.findall("\d", "h32rb17")
```

Esta vez, la lista sólo contiene cuatro elementos. Cada elemento es uno de los dígitos numéricos de la cadena.
### Símbolos para cuantificar ocurrencias

Otros símbolos cuantifican el número de ocurrencias de un carácter específico en el patrón. En un patrón de expresión regular, puede añadirlos después de un carácter o de un símbolo que identifique un tipo de carácter para especificar el número de repeticiones que coinciden con el patrón.

Por ejemplo, el símbolo `+` representa una o más repeticiones de un carácter específico. En el siguiente ejemplo, el patrón lo coloca después del símbolo `"\d"` para encontrar coincidencias con una o más apariciones de un solo dígito:

```python
import re

re.findall("\d+", "h32rb17")
```

Con la expresión regular `"\d+"`, la Lista contiene las dos coincidencias de `"32"` y `"17"`.

Otro símbolo utilizado para cuantificar el número de apariciones es el símbolo `*`. El símbolo `*` representa cero, una o más apariciones de un carácter específico. El código siguiente sustituye el símbolo `+` utilizado en el ejemplo anterior por el símbolo `*`. Puede ejecutarlo para examinar la diferencia:

```python
import re

re.findall("\d*", "h32rb17")

# Salida: ['', '32', '', '', '17', '']
```

Como también coincide con cero apariciones, la Lista contiene ahora cadenas vacías para los caracteres que no eran de un solo dígito.

Si desea indicar un número concreto de repeticiones a permitir, puede colocar este número entre llaves (`{ }`) después del carácter o símbolo. En el siguiente ejemplo, el patrón de expresión regular `"\d{2}"` indica a Python que devuelva todas las coincidencias de exactamente dos dígitos simples en una fila a partir de una cadena de varios ID de dispositivo:

```python
import re

re.findall("\d{2}", "h32rb17 k825t0m c2994eh")

# Salida: ['32', '17', '82', '29', '94']
```

Como coincide con dos repeticiones, cuando Python encuentra un dígito único, comprueba si hay otro a continuación. Si lo hay, Python añade los dos dígitos a la lista y pasa al siguiente. Si no lo hay, pasa al siguiente dígito sin añadir el primer dígito a la lista.

**Nota:** Python escanea las cadenas de izquierda a derecha cuando las compara con una expresión regular. Cuando Python encuentra una parte de la Cadena que coincide con el primer carácter esperado definido en la expresión regular, continúa comparando los caracteres siguientes con el patrón esperado. Cuando el patrón está completo, vuelve a comenzar este proceso. Así, en los casos en los que aparecen tres dígitos seguidos, trata el tercer dígito como un nuevo dígito de inicio.

También puede especificar un rango dentro de las llaves separando dos números con una coma. El primer número es el número mínimo de repeticiones y el segundo el número máximo de repeticiones. El siguiente ejemplo devuelve todas las coincidencias que tienen entre una y tres repeticiones de un solo dígito:

```python
import re

re.findall("\d{1,3}", "h32rb17 k825t0m c2994eh")

# Salida: ['32', '17', '825', '0', '299', '4']
```

La lista devuelta contiene elementos de un dígito como `"0"`, dos dígitos como `"32"` y tres dígitos como `"825"`.
### Construir un patrón

La construcción de una expresión regular requiere que descomponga el patrón que está buscando en trozos más pequeños y que represente esos trozos utilizando los símbolos que ha aprendido. Considere un ejemplo de una cadena que contiene múltiples datos sobre los empleados de una organización. Para cada empleado, la siguiente cadena contiene su ID de empleado, su nombre de usuario seguido de dos puntos (`:`), sus intentos de inicio de sesión del día y su departamento:

`employee_logins_string = "1001 bmoreno: 12 Marketing 1002 tshah: 7 Human Resources 1003 sgilmore: 5 Finance"`

Su tarea consiste en extraer el nombre de usuario y los intentos de inicio de sesión, sin el número de identificación del empleado ni su departamento.

Para completar esta tarea con expresiones regulares, necesita descomponer lo que está buscando en componentes más pequeños. En este caso, esos componentes son el número variable de caracteres de un nombre de usuario, dos puntos, un espacio y un número variable de dígitos simples. Los símbolos de expresión regular correspondientes son `\w+, :, \s y \d+` respectivamente. Utilizando estos símbolos como expresión regular, puede ejecutar el siguiente código para extraer las cadenas:

```python
import re

pattern = "\w+:\s\d+"

employee_logins_string = "1001 bmoreno: 12 Marketing 1002 tshah: 7 Human Resources 1003 sgilmore: 5 Finance"

print(re.findall(pattern, employee_logins_string))

# Salida: ['bmoreno: 12', 'tshah: 7', 'sgilmore: 5']
```

**Nota:** Trabajar con expresiones regulares puede conllevar el Riesgo de devolver información innecesaria o de excluir cadenas que desea devolver. Por lo tanto, es útil probar sus expresiones regulares.
## Puntos clave

Las expresiones regulares le permiten buscar en cadenas para encontrar coincidencias con patrones específicos. Puede utilizar expresiones regulares importando el módulo re. Este módulo contiene múltiples funciones, entre ellas re.findall(), que devuelve todas las coincidencias con un patrón en forma de lista. Para formar un patrón, se utilizan caracteres y símbolos. Los símbolos le permiten especificar tipos de caracteres y cuantificar cuántas repeticiones de un carácter o tipo de carácter pueden darse en el patrón.