---
Fecha: 2024-12-25
Categoría: Estructuras de datos básicas
tags:
  - front-end
  - curso-9
  - modulo-2
---
Esta lectura muestra la estructura de datos array, incluyendo cómo inicializar, gestionar y unir arrays. Todos los lenguajes de programación tienen alguna forma de array, pero su funcionamiento puede presentar ligeras diferencias. Por ejemplo, algunos lenguajes especifican que un array debe contener el mismo tipo de elemento, como un array string o un array int.

En cambio, otros lenguajes permiten almacenar elementos mixtos en una matriz. La funcionalidad de las matrices también puede diferir. A veces, un array será un objeto completo con una funcionalidad compleja. Al mismo tiempo, puede tratarse como un tipo de almacenamiento para primitivas; las operaciones y la funcionalidad se aplicarían entonces externamente.

## **1 Inicialización de arrays**
---
Las matrices pueden crearse de forma estática o dinámica. En un lenguaje estático, la matriz se mantendría en la pila y requeriría que el tipo de matriz se especificara _a priori_. Los lenguajes dinámicos ofrecen más fluidez, a veces piden que se fije el tamaño y no requieren que se especifique el tipo antes de su uso. Una instancia de este tipo se almacenaría en un montón. Las matrices tienen índices, que es un valor contiguo que comienza en 0 y aumenta hasta el final de la matriz. Cuando se necesita un elemento, se indica el nombre del array seguido de corchetes y la ubicación del índice.

`array_name[0]`

Este ejemplo recuperará el primer elemento de la matriz. Se puede utilizar cualquier número y se devolverá el elemento en esa ubicación de índice. Especificar un número mayor que el tamaño de la matriz arrojaría un error de fuera de límites. Una acción típica que realizará con una matriz es iterar sobre la matriz e investigar los elementos.

```
n <- size of array arr
FOR (i <- 0;i<(n-1); i <-(i+1)) DO
    process element arr[i]
END
```

La forma general de un for loop es la misma en todos los enfoques: se necesita el tamaño de la matriz, un número entero `i` que aumenta en cada iteración y un `for` loop general para la sintaxis. La apariencia puede variar ligeramente, pero el mecanismo subyacente es el mismo. Empezando en `0`, recorra cada elemento de la matriz y haga algo. Un array siempre tendrá alguna forma de acceder al tamaño. Algunos ejemplos son `.size()`, `len(array)` y `.length()`.

## **2 Gestión de matrices en memoria**
---
Una diferencia fundamental respecto a las matrices en los distintos lenguajes de programación es dónde se almacenan. Un elemento puede almacenarse en memoria de montón o de pila. ==La memoria de pila se crea al ejecutar una función. Se crea para esa función y se descarta después de la ejecución==. Los elementos de esta asignación de memoria sólo están disponibles para esa función. Por el contrario, ==la memoria de montón se crea durante la ejecución de las instrucciones y está disponible para todos==.

Debe tenerse cuidado al alterar elementos en un entorno estático. Al instanciar una matriz, se crea en la pila de llamadas un espacio de memoria igual al tamaño de inicialización especificado. Se crea una pila de llamadas para ejecutar el objetivo cuando se llama a una función. Alterar una matriz y devolverla de la pila puede dar lugar a que se corrompa la memoria, ya que la pila se descarta una vez finalizada la función.

Los lenguajes dinámicos evitan este problema almacenando el array en un montón. De este modo, la matriz no se ve afectada cuando finaliza la función y se descarta la pila. ==Las pilas, por su naturaleza, contienen bloques de memoria contiguos, lo que hace que el acceso a la información sea más manejable==. Un montón está menos organizado y puede llevar más tiempo acceder a los elementos. Una vez más, debe considerar el compromiso entre tamaño y comodidad, o accesibilidad frente a velocidad.

Normalmente, cuando un programa termina de utilizar un array, la memoria se desasigna y queda disponible para otra cosa. La forma en que se gestiona esta reasignación y la recogida de basura depende del lenguaje de programación seleccionado y sólo puede mejorar el rendimiento si se hace de forma eficaz. Una mala gestión de la memoria puede dar lugar a fugas, que pueden bloquear su aplicación en caso de llamadas repetidas.

Dos conceptos relacionados con la memoria que puede encontrar son la **copia superficial** y la **copia profunda**. La primera instancia no realiza una copia de la matriz, sino que devuelve una ubicación de índice. Una copia profunda creará una nueva instancia de un array. Hacer una copia superficial optimiza el uso de memoria; sin embargo, debe asegurarse de que no se realizan cambios inesperados de forma inadvertida en un array compartido por dos variables.

## **3 Unir matrices**

Una matriz es una matriz bidimensional (o una matriz compuesta de matrices) que puede actuar como una tabla. Puede utilizarse para representar filas y columnas. Da a un elemento una coordenada 2D (x,y). Aquí **x** se referiría a las filas e **y** a las columnas. Como antes, se utilizarían corchetes para acceder a un elemento de una matriz bidimensional. Sin embargo, para una matriz se necesitan dos posiciones de índice, como se indica a continuación.

`Matrix[x][y]`

Una matriz mostrará una forma cuadrada con el mismo número de columnas y filas. Esto no tiene por qué ser necesariamente así. Pero si decide no mantener la uniformidad, asegúrese de que su bucle actúa en consecuencia.

```python
int[][] matrix = new int[5][7]
for (int i = 0; i < matrix.length; i++) {
    for(int j = 0; j < matrix[i].length; j++)
    {
        doSomethingNeo(matrix[i][j])
    }
}
```

En este ejemplo, se inicializa una matriz 2D denominada matrix para contener números enteros. La colección exterior puede contener cinco elementos (matrices de enteros). Las matrices interiores tienen todas una capacidad de 7. La primera matriz de la matriz exterior se selecciona con el `i`, se determina el tamaño (7) y, a continuación, se pasa cada elemento de esa matriz interior al método. ==Observe cómo se ha accedido dinámicamente al tamaño del array interior mediante el atributo `.length`==. Esto garantiza que no pueda haber errores fuera de los límites durante la iteración.

## **Conclusión**

Las matrices son una estructura de datos fundamental que existe en la mayoría de los lenguajes de programación. Ayudan a almacenar datos relacionados. Cabe señalar que su implementación varía en función del lenguaje, por lo que debe tenerse cuidado al utilizarlas. Esta lectura le ha enseñado la estructura de datos array, incluyendo cómo inicializar, gestionar y unir arrays.