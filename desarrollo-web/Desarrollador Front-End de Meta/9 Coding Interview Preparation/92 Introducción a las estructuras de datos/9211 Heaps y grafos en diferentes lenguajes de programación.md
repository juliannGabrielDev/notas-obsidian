---
Fecha: 2024-12-26
Categoría: Estructuras de datos avanzadas
tags:
  - front-end
  - curso-9
  - modulo-2
---
- [[#Introducción|Introducción]]
- [[#1 Terminología|1 Terminología]]
- [[#2 NetworkX|2 NetworkX]]
- [[#3 Heaps|3 Heaps]]
- [[#Conclusión|Conclusión]]

## Introducción
---
En esta lectura, la atención se centra en los **grafos** y los **montones**. Un grafo es una estructura de datos no lineal que puede almacenar información de forma que permita extraer algunas relaciones interesantes que se encuentran en los datos. Los montones pueden definirse como grafos especializados que conceden especial importancia al elemento superior.

## 1 Terminología
---
Los grafos se componen de nodos y aristas. El nodo es donde se almacenan los datos, y la arista es una conexión entre dos nodos. A diferencia de un árbol, los nodos no tienen que estar conectados y pueden existir independientemente de los demás nodos. Una arista conecta dos nodos. Se puede decir que una arista tiene un peso. Se trata de un valor que se almacena en la conexión y que infiere cierta información sobre la fuerza de la conexión entre los dos nodos. Se puede decir que un grafo es dirigido, esto significa que las aristas son dirigidas (como una calle de un solo sentido) o no dirigidas (como una calle de dos sentidos) y la conexión infiere información de ida y vuelta.

## 2 NetworkX
---
NetworkX es una biblioteca externa basada en Python que puede importarse al entorno Python y utilizarse para modelar datos. Se trata de una biblioteca externa ligera que puede funcionar en cualquier entorno Python. Entre sus muchas funciones se incluyen los grafos dirigidos, no dirigidos, cíclicos y acíclicos. NetworkX también es compatible con una amplia gama de algoritmos basados en grafos, entre los que se incluyen:

- Métricas de distancia (la distancia entre dos nodos)
- Centralidad (lo central que es un nodo en relación con otros nodos)
- Y detección de camarillas (se refiere a subconjuntos dentro de un grafo)

Un algoritmo de detección de camarillas analizará un gráfico para determinar una serie de subconjuntos con más probabilidades de tener relaciones internas fuertes y externas débiles. Se denominan camarillas debido a su parecido con las camarillas sociales. Esta puede ser una forma útil de identificar clientes potencialmente relacionados, dada una muestra de datos y hábitos de clientes. NetworkX puede modelarse utilizando matplotlib de Python para dar una idea de los descubrimientos de los datos. Esto se utiliza como una aplicación back-end por un programador que interroga a los datos en busca de insights.

## 3 Heaps
---
Los heaps se implementan de forma diferente en los distintos lenguajes, pero son esencialmente grafos con restricciones específicas. Los heaps clasifican la información en orden para poder devolver rápidamente valores mínimos y máximos. Así, emplean un enfoque binario, y cualquier implementación debe tener un máximo de dos nodos. Dependiendo de la implementación, un montón tendrá como raíz el valor más grande o el más pequeño. Por último, cada rama del montón seguirá un patrón secuencial.

Un montón tiene un tiempo de búsqueda `O(1)` porque sólo devuelve un elemento. El valor más alto o más bajo depende de si se trata de un montón min o max. Esto significa que una vez que se extrae este valor, el siguiente elemento se coloca en el nodo raíz del montón. Esto también afecta a la inserción en un montón. Cuando se añade un nuevo elemento, empezando por la raíz, se compara con cada nodo hasta determinar la posición correcta. A continuación, se mueven los elementos circundantes para garantizar que se coloca en la posición adecuada.

Una forma alternativa que algunos lenguajes como Kotlin o Javascript. que carecen de una instancia incorporada, representan los montones utilizando una lista de arrays. Se emplean las mismas propiedades que se utilizan con los grafos, aunque la implementación real puede diferir ligeramente. La eficacia de los montones dependerá de la estructura de datos subyacente utilizada, por lo que merece la pena investigar la eficacia de la implementación de su lenguaje de destino antes de utilizarlos.

## Conclusión
---
En esta lectura se han revisado los grafos y los montones. Los montones pueden verse como grafos especializados, y un grafo se compone de nodos y aristas. Existen algunos métodos muy especializados para grafos, cuyo propósito es permitirnos inferir alguna conexión a partir de los datos que se almacenan en ellos.