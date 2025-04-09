- Numérico
	- Integer
	- Float
	- Número complejo
- Sequencia
	- String
	- Listas `[]`
	- Tuplas `()`: Inmutable
- Diccionario `{"a": 10, "b": 10}`
- Booleano
- Set `{"hola", 4, 4.5}`

- [[#Obtener el tipo de dato|Obtener el tipo de dato]]
- [[#Conversión a otro tipo|Conversión a otro tipo]]
	- [[#Conversión a otro tipo#Entero y flotante|Entero y flotante]]
	- [[#Conversión a otro tipo#Cadena|Cadena]]
	- [[#Conversión a otro tipo#Booleano|Booleano]]
	- [[#Conversión a otro tipo#Conversión Entre Colecciones|Conversión Entre Colecciones]]

---
## Obtener el tipo de dato

```python
print(type("Hola")) # <class 'str'>
```

## Conversión a otro tipo

### Entero y flotante

- La función `int()` convierte valores en números enteros
- `float()` lo hace a números de punto flotante.

### Cadena

- La función `str()` convierte valores de otros tipos en cadenas.

### Booleano

- Con `bool()` transformas valores a `True` o `False`.

```python
print(bool(0))         # Salida: False
print(bool("Hola"))    # Salida: True
print(bool([]))        # Salida: False
```

### Conversión Entre Colecciones

Funciones como `list()`, `tuple()`, `dict()` y `set()` permiten convertir entre diferentes tipos de colecciones.