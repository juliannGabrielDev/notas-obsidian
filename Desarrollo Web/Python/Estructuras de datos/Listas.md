Las listas son una de las estructuras de datos más versátiles en Python. Son colecciones ordenadas de elementos. Aquí te presento una descripción básica de las listas y algunos de sus métodos más comunes:

### ¿Qué es una Lista?

- Los elementos pueden ser de diferentes tipos (números, texto, ¡incluso otras listas!).
- Los elementos en una lista están ordenados, lo que significa que tienen una posición específica.
- Las listas son _mutables_, lo que significa que puedes cambiar su contenido después de crearlas.
- Se crean usando corchetes `[]` y separando los elementos con comas.

```python
mi_lista = [1, 2, "hola", 3.14, True]
```

### Métodos Comunes de Listas

Aquí tienes una tabla con algunos de los métodos de listas más utilizados:

|Método|Descripción|Ejemplo|
|---|---|---|
|`append(elemento)`|Añade un elemento al final de la lista.|`mi_lista.append(4)`|
|`extend(iterable)`|Añade todos los elementos de un iterable (como otra lista) al final de la lista.|`mi_lista.extend([5, 6, 7])`|
|`insert(índice, elemento)`|Inserta un elemento en un índice específico.|`mi_lista.insert(2, 10)`|
|`remove(elemento)`|Elimina la primera aparición de un elemento de la lista.|`mi_lista.remove(3)`|
|`pop(índice=-1)`|Elimina y devuelve el elemento en el índice especificado (o el último elemento si no se especifica el índice).|`elemento_eliminado = mi_lista.pop(1)`|
|`clear()`|Elimina todos los elementos de la lista.|`mi_lista.clear()`|
|`index(elemento, inicio=0, fin=len(lista))`|Devuelve el índice de la primera aparición de un elemento en la lista (o lanza un `ValueError` si el elemento no está presente).|`índice = mi_lista.index(2)`|
|`count(elemento)`|Devuelve el número de veces que aparece un elemento en la lista.|`conteo = mi_lista.count(2)`|
|`sort(key=None, reverse=False)`|Ordena los elementos de la lista en su lugar (de forma predeterminada, en orden ascendente).|`mi_lista.sort()`|
|`reverse()`|Invierte el orden de los elementos de la lista en su lugar.|`mi_lista.reverse()`|
|`copy()`|Devuelve una copia superficial de la lista.|`copia_lista = mi_lista.copy()`|