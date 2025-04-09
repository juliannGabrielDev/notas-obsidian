El bucle `for` en Python permite iterar sobre una secuencia de elementos, como una lista, tupla o cadena. Permite ejecutar un bloque de código repetidamente para cada elemento de la secuencia.

## Sintaxis básica

La sintaxis básica del bucle `for` es la siguiente:

```python
for elemento in secuencia:
    # código a ejecutar para cada elemento
```

La variable `elemento` toma el valor de cada elemento de la secuencia en cada iteración. El bloque de código dentro del bucle se ejecuta una vez para cada elemento.

## Ejemplos

Aquí tienes algunos ejemplos para ilustrar el uso del bucle `for`:

```python
# Iterar sobre una lista
frutas = ["manzana", "plátano", "cereza"]
for fruta in frutas:
    print(fruta)

# Iterar sobre una cadena
mensaje = "Hola"
for letra in mensaje:
    print(letra)

# Iterar sobre un rango de números
for i in range(5):
    print(i)

# Iterar sobre una tupla de tuplas
puntos = [(1, 2), (3, 4), (5, 6)]
for x, y in puntos:
    print(f"x = {x}, y = {y}")
```

## Funciones útiles

Hay algunas funciones útiles que se pueden utilizar con el bucle `for`:

- `range()`: genera una secuencia de números.
- `enumerate()`: devuelve una tupla que contiene el índice y el valor de cada elemento de la secuencia.
- `zip()`: combina dos o más secuencias en una sola secuencia de tuplas.

Aquí tienes algunos ejemplos:

```python
# Usar enumerate() para obtener el índice y el valor
frutas = ["manzana", "plátano", "cereza"]
for indice, fruta in enumerate(frutas):
    print(f"Índice: {indice}, fruta: {fruta}")

# Usar zip() para combinar dos listas
nombres = ["Juan", "María", "Pedro"]
edades = [25, 30, 35]
for nombre, edad in zip(nombres, edades):
    print(f"{nombre} tiene {edad} años")
```