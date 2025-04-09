Los conjuntos (sets) en Python son colecciones desordenadas de elementos únicos. Aquí tienes una descripción general de los conjuntos:

**Características clave:**

- **Desordenados:** Los elementos de un conjunto no tienen un orden específico.
- **Únicos:** Los conjuntos no permiten elementos duplicados.
- **Mutables:** Se pueden agregar y eliminar elementos de un conjunto después de su creación.
- **No indexados:** No se puede acceder a los elementos de un conjunto mediante índices.
- **Se definen con llaves:** Los conjuntos se crean encerrando los elementos entre llaves `{}`, separados por comas.

**Ejemplos de uso:**

```python
# Creación de conjuntos
conjunto1 = {1, 2, 3, 4, 5}
conjunto2 = {"manzana", "banana", "cereza"}
conjunto3 = {True, False, True}

# Agregar elementos
conjunto1.add(6)
print(conjunto1)

# Eliminar elementos
conjunto1.remove(3)
print(conjunto1)

# Operaciones de conjuntos
conjunto_union = conjunto1.union(conjunto2)
print(conjunto_union)

conjunto_interseccion = conjunto1.intersection({4, 5, 6})
print(conjunto_interseccion)

conjunto_diferencia = conjunto1.difference({4, 5, 6})
print(conjunto_diferencia)
```