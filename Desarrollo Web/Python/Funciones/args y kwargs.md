`*args` y `**kwargs` son herramientas en Python que te permiten crear funciones más flexibles al aceptar un número variable de argumentos.

## `*args` (Argumentos posicionales variables)

- `*args` se utiliza para pasar un número variable de argumentos posicionales a una función.
- Los argumentos se recopilan en una tupla dentro de la función.
- El nombre `args` es una convención; puedes usar cualquier nombre válido, pero el asterisco (`*`) es esencial.

```python
def sumar(*numeros):
    total = 0
    for numero in numeros:
        total += numero
    return total

print(sumar(1, 2, 3))  # Salida: 6
print(sumar(1, 2, 3, 4, 5))  # Salida: 15
```

## `**kwargs` (Argumentos de palabras clave variables)

- `**kwargs` se utiliza para pasar un número variable de argumentos de palabras clave (con nombre) a una función.
- Los argumentos se recopilan en un diccionario dentro de la función, donde las claves son los nombres de los argumentos y los valores son los valores de los argumentos.
- El nombre `kwargs` es una convención; puedes usar cualquier nombre válido, pero el doble asterisco (`**`) es esencial.

```python
def mostrar_informacion(**datos):
    for clave, valor in datos.items():
        print(f"{clave}: {valor}")

mostrar_informacion(nombre="Ana", edad=30, ciudad="México")
# Salida:
# nombre: Ana
# edad: 30
# ciudad: México
```