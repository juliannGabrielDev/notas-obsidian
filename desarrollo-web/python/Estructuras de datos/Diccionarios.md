Los diccionarios son colecciones desordenadas de pares clave-valor. Cada clave es única dentro de un diccionario, y está asociada a un valor específico. Los diccionarios son mutables, lo que significa que puedes modificar, agregar o eliminar elementos después de su creación.

**Características clave:**

- **Pares clave-valor:** Los diccionarios almacenan datos en forma de pares clave-valor.
- **Claves únicas:** Cada clave en un diccionario debe ser única.
- **Mutabilidad:** Los diccionarios se pueden modificar después de su creación.
- **Desordenados:** Los diccionarios no mantienen un orden específico de los elementos.
- **Indexación por claves:** Se accede a los valores en un diccionario mediante sus claves, no por índices.

**Cómo crear diccionarios:**

- **Usando llaves {}:**
```python
mi_diccionario = {"nombre": "Juan", "edad": 30, "ciudad": "Madrid"}
```

- **Usando la función `dict()`:**
```python
mi_diccionario = dict(nombre="Juan", edad=30, ciudad="Madrid")
```

## Operaciones comunes:

Obtener claves, valores o pares clave-valor:

```python
claves = mi_diccionario.keys()
valores = mi_diccionario.values()
pares = mi_diccionario.items()
```

Verificar la existencia de una clave:

```python
if "nombre" in mi_diccionario:
    print("La clave 'nombre' existe.")
```