---
Fecha: 2024-12-26
Categoría: Clasificación y búsqueda
tags:
  - front-end
  - curso-9
  - modulo-3
---
- [[#1 Ordenación por selección|1 Ordenación por selección]]
- [[#2 Ordenación rápida|2 Ordenación rápida]]
- [[#Conclusión|Conclusión]]

Anteriormente aprendió que la complejidad temporal y espacial es un medio para evaluar la eficiencia del código. En esta lectura, explorará la complejidad temporal y espacial de los algoritmos de ordenación por selección y ordenación rápida. Estos son algoritmos comunes que se utilizan para ordenar datos en un array.

## 1 Ordenación por selección
---
La ordenación por selección es un algoritmo de ordenación que funciona a partir de un principio muy simple. ==Toma un array e itera de izquierda a derecha. Empezando por el primer lugar del índice, itere sobre toda la matriz e intercambie este valor con el valor más bajo que se encuentre a la derecha de este elemento==. Repita la operación hasta que todo el array esté ordenado.

La ordenación por selección tiene:

- La complejidad temporal en el peor de los casos es O(N^2)
- La complejidad temporal del caso medio es O(N^2)
- La complejidad temporal en el mejor de los casos es O(N^2)
- Complejidad espacial: O(1) _Auxiliar_.

Para realizar la ordenación por selección, siga los siguientes pasos:

- Encuentre el valor más pequeño e intercámbielo con el primer valor de la matriz
- Encuentre el segundo valor más pequeño e intercámbielo con el segundo lugar de la matriz
- Repita el proceso hasta que todos los elementos estén ordenados del más pequeño al más grande.

La complejidad temporal se determina en función del número de operaciones realizadas. Dada una lista de tamaño n, el compilador debe buscar en cada entrada de la lista para identificar el elemento más pequeño y, a continuación, realizar un intercambio a la posición de índice 0. El pseudocódigo del algoritmo es el siguiente.

```
for(i = 0; i < n-1; i++)
int min_index = i
    for(j = i+1; j < n; j++)
        if(List[j] < List[min_index])
            min_index=j 
    swap(List[i], List[min_index])
```

La línea 1 dice que la longitud de la lista `List` debe buscarse `n-1` veces. La línea 2 establece una variable temporal para mantener el valor más bajo. La línea 3 es un bucle interno que debe iterar a través del bucle `n-1` veces. La línea 4 comprueba si el valor encontrado en la posición `List[j]` es menor que el valor más bajo actual. Si es así, se registra la posición de ese elemento. Al final de cada bucle interno, el valor encontrado como el más bajo se intercambia con la posición `i` en el índice, `i` se incrementa y el procedimiento comienza de nuevo. Compruebe siempre el siguiente elemento de la lista hasta que se hayan comprobado todos los elementos.

Hay cuatro consideraciones a tener en cuenta al evaluar este algoritmo.

1. **El peor de los casos**: Dada una lista ordenada en orden inverso, ¿cuántas comparaciones se realizan? El bucle interior y exterior tendrán que ejecutarse `n` veces, por lo que puede determinarse que en el peor de los casos = `O(n^2)`.
2. **Comparación media**: Independientemente del orden de la lista, cada elemento debe compararse con el caso medio = `O(n^2)`.
3. `Mejor comparación`: Dada una lista ordenada, cuántas comparaciones deben realizarse. De nuevo, independientemente de los elementos de la lista, cada elemento debe ser comprobado, por lo que el mejor caso = `O(n^2)`.
4. Por último, ¿cuál es la complejidad espacial de este enfoque? Dado que se está realizando un intercambio in situ, no se requiere ninguna matriz temporal. Hay tres variables temporales i, j y min_index; sin embargo, éstas no dependen del tamaño de la lista. Por lo tanto, la imagen duplica la lista y la complejidad espacial no aumenta en consecuencia. Por lo tanto, la complejidad espacial = `O(1)`.

Al evaluar la complejidad temporal, una buena regla general es considerar qué ocurrirá si se duplica la lista. Naturalmente, los bucles interior y exterior tendrán que aumentar en ninguna iteración para ajustarse a los elementos adicionales de la lista. Por lo tanto, se puede concluir que la complejidad temporal aumenta con el tamaño.

## 2 Ordenación rápida
---
*Quicksort* es un enfoque de ordenación que utiliza una metodología de dividir y conquistar. Dada una matriz de elementos, se determina un lugar en la matriz en el que dividir la matriz y que se denomina punto de `pivote`. Todos los valores mayores que este punto van a la derecha y todos los valores menores que este punto van a la izquierda. En este paso, usted tiene dos arrays. Se aplica el mismo proceso a estas matrices hasta que no queden elementos por ordenar.

Quicksort tiene:

- Complejidad temporal en el peor de los casos `O(n^2)`
- Complejidad temporal en el caso medio `O(n log n)`
- Complejidad temporal en el mejor de los casos `O(n log n)`
- Complejidad espacial `O(n)`

Para realizar el ordenamiento rápido, siga los siguientes pasos:

- Seleccione un punto de la lista sobre el que pivotar.
- Divida la lista en dos listas, los elementos a la izquierda del pivote y los elementos a la derecha.
- Establezca la variable `i` para iterar de izquierda a derecha sobre la izquierda del pivote. Establezca la variable `j` para que itere de derecha a izquierda en la parte izquierda del pivote.
- Las variables `i` a la izquierda buscan un valor mayor o igual que el pivote. Las variables `j` a la derecha buscan un valor menor o igual que el pivote.
- Cuando `j < i`, los valores en estas posiciones de índice se intercambian, esto se repite hasta que `i` y `j` se encuentran en el punto de pivote.
- Divida los valores de la lista en dos listas, una a la izquierda y otra a la derecha del pivote. Repita el proceso en cada una de las matrices resultantes.
- Aplique recursivamente el algoritmo.

El pseudocódigo siguiente para el ordenamiento rápido se realiza de forma recursiva.

- Empezando por el elemento situado más a la izquierda, se comprueba cada elemento posterior y, si se encuentra que es menor, se intercambia.
- La línea 3 llama al método de partición, que comienza en la línea 8.
- La línea 10 determina el elemento más significativo que se colocará a la derecha de la lista. La línea 10 establece una variable `i` que se asigna al índice del elemento más pequeño. La variable `j` se utiliza entonces para comprobar los elementos situados a la derecha a partir de los cuales realizar una comparación con el elemento más pequeño actual.
- La línea 12 determina si va a haber un intercambio, un elemento más pequeño a la derecha requerirá moverse a la posición del índice actual. La línea `4` es para ordenar el array izquierdo.
- La línea 5 es para ordenar el array derecho. En cada iteración, el tamaño del array a ordenar se reduce a la mitad. Las matrices se descompondrán continuamente hasta que sólo quede un elemento en las submatrices. El resultado de llamar a partición determinará la ubicación del elemento actual. Esta ubicación se incrementa y se repite hasta que cada elemento descanse en su posición naturalmente ordenada.

```
QuickSort(List, low, high)
        if(low<high) 
	pivot=partition(List, high, low)
	QuickSort(List, how, pivot-1)
	QuickSort(List, pivot+1, high) 

Partition(List,high,low)
        pivot=arr[high]
        i=(low-1)
        for j = low; j <= high-1; j++) 
	if(List[j] < pivot)
	        i++
	        swap(List[i], List[j]) 
        swap(arr[i+1], List[j]) 
        return I + 1 
```
​
Aspectos a tener en cuenta al evaluar este algoritmo:

1. En el peor de los casos: esto ocurre cuando el elemento más significativo se elige sistemáticamente como punto de pivote. Esto provocará un bucle para iterar sobre cada elemento `n` desde la izquierda. La división provocará una búsqueda de cada elemento de la derecha sin ninguno de la izquierda, `O(n^2)`.
2. Caso medio: se selecciona un punto de pivote medio en cada llamada. Esto reducirá el número de iteraciones adicionales necesarias. Así, habrá `n` iteraciones y un número cada vez menor de `logn` llamadas iterativas, `O(n*logn)`.
3. En el mejor de los casos: Siempre se selecciona el valor medio y el espacio de iteración se reduce a la mitad en cada iteración, `O(n*logn)`.
4. La naturaleza iterativa del algoritmo repercutirá en la complejidad del espacio porque la llamada a la función y las variables se mantienen en la pila mientras se realizan los cálculos. Sin embargo, la decisión de utilizar un intercambio in situ significa que no es necesario crear una nueva matriz, `O(log n)`.

## Conclusión
---
Se han desglosado y analizado dos enfoques de ordenación diferentes a través de la lente del espacio y la complejidad de Big-O. Se ha demostrado que la ordenación rápida es más compleja en su implementación pero devuelve soluciones globalmente más rápidas. La ordenación por selección es más simplista y menos pesada en cuanto a código y requiere menos espacio, pero no generará resultados con la misma eficacia.

En esta lectura, ha explorado la complejidad temporal y espacial de los algoritmos de ordenación por selección y ordenación rápida.