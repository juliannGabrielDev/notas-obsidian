El bucle `while` en Python es una estructura de control que permite ejecutar un bloque de código repetidamente mientras una condición sea verdadera.

## Sintaxis básica

La sintaxis básica del bucle `while` es la siguiente:

```python
while condición:
    # código a ejecutar mientras la condición sea verdadera
```

## Ejemplos

Aquí tienes algunos ejemplos para ilustrar el uso del bucle `while`:

```python
# Imprimir números del 1 al 5
i = 1
while i <= 5:
    print(i)
    i += 1

# Pedir al usuario que ingrese un número positivo
número = int(input("Ingresa un número positivo: "))
while número <= 0:
    número = int(input("Número inválido. Ingresa un número positivo: "))

# Simular un bucle infinito (con cuidado)
while True:
    respuesta = input("¿Quieres continuar? (s/n): ")
    if respuesta == "n":
        break  # Salir del bucle
```