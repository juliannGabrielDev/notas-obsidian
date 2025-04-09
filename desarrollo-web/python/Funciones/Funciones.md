Las funciones son bloques de código reutilizables que realizan tareas específicas.

```python
def nombre_de_la_función(parámetros):
    """Documentación de la función (opcional)"""
    # Cuerpo de la función
    return valor_de_retorno (opcional)
```

## Ejemplos

Aquí tienes algunos ejemplos para ilustrar el uso de funciones en Python:

```python
# Función sin parámetros ni valor de retorno
def saludar():
    print("¡Hola, mundo!")

# Función con parámetros y valor de retorno
def sumar(a, b):
    """Suma dos números y devuelve el resultado."""
    resultado = a + b
    return resultado

# Llamadas a las funciones
saludar()  # Imprime "¡Hola, mundo!"
suma = sumar(5, 3)  # Devuelve 8
print(suma)  # Imprime 8
```

## Tipos de funciones

En Python, existen diferentes tipos de funciones:

- **Funciones integradas**: son funciones que ya están definidas en Python, como `print()`, `len()`, `sum()`, etc.
- **Funciones definidas por el usuario**: son funciones que se definen utilizando la palabra clave `def`, como en los ejemplos anteriores.
- **Funciones anónimas (lambda)**: son funciones pequeñas y anónimas que se definen con la palabra clave `lambda`.