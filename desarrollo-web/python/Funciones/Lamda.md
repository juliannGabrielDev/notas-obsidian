## ¿Qué son las funciones lambda?

En esencia, las funciones lambda son funciones anónimas, lo que significa que no tienen un nombre asignado. Se definen utilizando la palabra clave `lambda`, seguida de una lista de argumentos, dos puntos (`:`) y una expresión que se evalúa y devuelve como resultado.

## Sintaxis

La sintaxis básica de una función lambda es la siguiente:

```python
lambda argumentos: expresión
```

## Ejemplos

Aquí tienes algunos ejemplos para ilustrar el uso de funciones lambda:

```python
# Función lambda para sumar dos números
suma = lambda a, b: a + b
resultado = suma(5, 3)  # Resultado: 8

# Función lambda para elevar un número al cuadrado
cuadrado = lambda x: x**2
resultado = cuadrado(4)  # Resultado: 16

# Función lambda para verificar si un número es par
es_par = lambda x: x % 2 == 0
resultado = es_par(7)  # Resultado: False
resultado = es_par(8) # Resultado: True

# Función lambda para obtener la primera letra de un string.
primera_letra = lambda string: string[0]
resultado = primera_letra("Hola") # Resultado: "H"
```