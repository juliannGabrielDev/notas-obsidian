---
Fecha: 2024-12-26
Categoría: Clasificación y búsqueda
tags:
  - front-end
  - curso-9
  - modulo-3
---
- [[#1 Búsqueda lineal|1 Búsqueda lineal]]
- [[#2 Búsqueda binaria|2 Búsqueda binaria]]
- [[#Conclusión|Conclusión]]

En esta lectura, explorará la complejidad temporal y espacial en los algoritmos de búsqueda lineal y binaria. Para tener una idea más clara de cómo se caracteriza la complejidad temporal y espacial, se examinan estas dos búsquedas observando el tiempo y el espacio empleados en encontrar el elemento objetivo.

## 1 Búsqueda lineal
---
Una búsqueda lineal es la forma más directa de recuperar un elemento. Significa que la búsqueda comienza en el primer elemento e itera hasta que se encuentra el elemento objetivo o no quedan más elementos en la matriz que comprobar.

Dada una lista de números, comience en la posición índice 0 y compare cada elemento con una variable objetivo. Devuelve cuando se ha determinado la ubicación del índice o se ha comprobado toda la lista y no hay ninguna instancia del elemento objetivo.

![[busqueda-lineal.webp]]

Estos son los resultados a tener en cuenta al evaluar la eficacia de la búsqueda.

- **En el peor de los casos**: El elemento está ausente de la lista. Para determinarlo, hay que buscar en todas las ubicaciones posibles de la lista de tamaño `n`. `O(n)` complejidad temporal.
- **Caso medio**: El elemento se encuentra en el centro. Esto se considera un resultado de `O(n)`.
- **Mejor caso**: El elemento se encuentra en el índice inicial y no se requieren más comprobaciones, por lo que `O(1)`.
- **Complejidad espacial**: No se requiere espacio adicional para realizar la búsqueda. Por lo tanto, el espacio necesario sólo será tan grande como los elementos que haya que almacenar en la lista, complejidad espacial `O(n)`.

## 2 Búsqueda binaria
---
Una búsqueda binaria se realiza identificando primero el punto medio en una lista ordenada, comparando el elemento objetivo con él y descartando la mitad que sea menor que el elemento objetivo. Esta división por la mitad en el punto medio se repite hasta que se encuentra el elemento objetivo o no hay más lista que dividir por la mitad.

Para realizar una búsqueda binaria, primero hay que ordenar la lista.

![[busqueda-binaria.webp]]

En primer lugar, se selecciona un punto medio. El valor en el índice 3, es 15. ¿Es mayor o menor que el elemento objetivo? El espacio de búsqueda se divide en dos y se sigue examinando el de la izquierda.

![[busqueda-binaria-2.webp]]

Se selecciona un nuevo punto central. Esta vez sólo hay tres ranuras que comprobar; la posición del índice 1 está en el punto medio.

![[busqueda-binaria-3.webp]]

El valor objetivo se encuentra aquí y no se requieren más divisiones.

estos son los resultados que hay que tener en cuenta para evaluar la eficacia de la búsqueda:

- **Peor caso**: El elemento está ausente de la lista. Debido a la naturaleza del planteamiento, muchos elementos se eliminan con el uso de los operadores lógicos mayor que y menor que. Esto significa que sólo se comprueba primero `n/2` , después `n/4` y `n/8`. La complejidad global es entonces `O(log n)`.
- **Caso medio**: El elemento se encuentra tras varias iteraciones. De nuevo, debido al mecanismo de búsqueda, cada llamada posterior reduce el espacio de estados. Así, se puede determinar que tras un número medio de búsquedas, la complejidad es `O(Log n)`.
- **Mejor caso**: El elemento se encuentra en el índice inicial y no se requieren más comprobaciones, por lo que `O(1)`.
- **Complejidad espacial**: No se requiere espacio adicional para realizar la búsqueda. Por lo tanto, el espacio necesario sólo será tan grande como los elementos que haya que almacenar en la lista, complejidad espacial `O(n)`.

## Conclusión
---
En esta lectura, ha explorado la complejidad temporal y espacial de los algoritmos de búsqueda lineal y binaria. Se ha analizado la complejidad temporal y espacial de la búsqueda lineal y binaria. Ambos enfoques son búsquedas in situ; por lo tanto, no se requiere espacio adicional, por lo que la complejidad espacial es pequeña. La búsqueda lineal ha demostrado ser más compleja en el tiempo en todos los casos, aparte de que el elemento correcto se encuentra en el primer intento.

La búsqueda binaria reduce a la mitad el espacio de estados en cada iteración, lo que la hace mucho más eficiente. Sin embargo, debe tener en cuenta el tiempo necesario para ordenar la matriz en los cálculos globales cuando evalúe la eficacia de seleccionar este enfoque para una aplicación general.
