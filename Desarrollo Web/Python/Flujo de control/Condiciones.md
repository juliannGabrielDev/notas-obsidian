## Declaración if

```python
x = 10
if x > 5:
    print("x es mayor que 5")
```

## Declaración else

```python
x = 2
if x > 5:
    print("x es mayor que 5")
else:
    print("x no es mayor que 5")
```

## Declaración elif

```python
x = 5
if x > 5:
    print("x es mayor que 5")
elif x < 5:
    print("x es menor que 5")
else:
    print("x es igual a 5")
```

## Operadores lógicos

También puedes combinar varias condiciones mediante operadores lógicos:

- `and` (verdadero si ambas condiciones son verdaderas)
- `or` (verdadero si al menos una condición es verdadera)
- `not` (invierte el valor de una condición)

## Condicionales ternarios

Los condicionales ternarios son una forma concisa de escribir declaraciones `if-else` en una sola línea.

```python
x = 10
mensaje = "x es mayor que 5" if x > 5 else "x no es mayor que 5"
print(mensaje)
```