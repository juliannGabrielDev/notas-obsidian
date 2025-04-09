---
Fecha: 2024-12-24
Categoría: Fundamentos de Figma
tags:
  - front-end
  - curso-7
  - modulo-3
---
## **1 Capas**
---
Los documentos Figma pueden llegar a ser excesivamente complejos porque suelen contener una densa combinación de imágenes, objetos y texto. Los diseñadores a veces se ven tentados a dejar su panel de capas con un aspecto de caos organizado, lo que dificulta encontrar las cosas.

## **2 Enfoques de denominación de capas**
---
Cuándo y hasta qué punto nombramos nuestras capas depende de la madurez de nuestro diseño y de la fase del proceso de diseño en la que nos encontremos (ideación, colaboración, listo para el traspaso).

## **3 Convenciones**
---
Dado que cada equipo es único, los consejos de esta lectura son sólo eso: consejos. En función de la legibilidad o de cómo prefiera el equipo de desarrolladores estructurar sus componentes, puede desarrollar sus propios métodos de trabajo. La persona que nombre las capas también vendrá determinada por la fase de su proceso de diseño, el tamaño de su equipo y el nivel de implicación de sus desarrolladores en el proceso de diseño. Para empezar, he aquí algunos métodos:

## **4 Ideación en la fase de diseño**

En este paradigma, no hay necesidad de nombrar capas porque usted todavía está en modo de flujo libre, generando ideas y centrándose primero en resolver el problema.

En este punto sólo nos estamos divirtiendo, por lo que no necesitamos preocuparnos por la nomenclatura o la estructura de las capas. El creador de archivos hace la nomenclatura por usted. Como esto es todavía muy scrappy, no se preocupe por la nomenclatura o incluso por el uso de elementos específicos (¡quizás un rectángulo sea suficiente para un botón!).

## **5 Perfeccionamiento**
---
Cuando usted y su equipo se estén preparando para la aprobación de sus principales interesados, es cuando querrá pensar en lo fácil que es para alguien digerir sus ideas e iterar sobre ellas, una clara denominación de las capas ayuda mucho en esto.

Utilice nombres de capas descriptivos. Una tarjeta debe llamarse tarjeta, un número debe llamarse número y una descripción debe llamarse descripción. En este punto, usted sigue siendo el propietario de sus diseños pero está intercambiando ideas con sus colegas. Este es un momento excelente para nombrar las capas de modo que tengan sentido como grupo. La forma más sencilla de conseguirlo es ser lo más descriptivo posible.

## **6 Grupos y marcos**

Cuando trabaje con un gran número de capas, necesitará un método más formal para agruparlas. En otro software de diseño, utilizaría un grupo para ello, pero Figma le ofrece otra opción: los marcos. Los marcos parecen muy similares a los grupos a primera vista, así que echemos un vistazo más de cerca y descubramos sus características únicas.

Empecemos por lo fundamental. Todas las aplicaciones gráficas tienen ahora la funcionalidad de agrupar: seleccione algunos objetos, pulse Comando G en Mac o Ctrl G en Windows, y su lista de capas tendrá ahora un aspecto más limpio con un grupo plegable. Los grupos se definen por su contenido. Los límites de su grupo son los bordes exteriores de lo que haya dentro de él. Como resultado, siempre que cambie la posición o las dimensiones de un objeto, los límites del grupo cambiarán en consecuencia. El elemento padre de su documento está relacionado con el objeto del grupo. Las restricciones del grupo se establecen por defecto en "*Izquierda*" y "*Arriba*", como muestran las líneas discontinuas aquí:

Si las restricciones se establecen a escala, su grupo se escalará con su elemento padre. Cuando redimensiona un grupo, el contenido siempre se redimensiona también. Puede mantener la misma relación de aspecto manteniendo pulsada la tecla Mayús mientras redimensiona.

## **7 Marcos**
---
A primera vista, no parece haber mucha distinción entre los grupos y los marcos. Usted selecciona sus objetos y pulsa Comando G en Mac o Ctrl-Alt-G en Windows para convertirlos en un marco. Se contraerán de forma similar en la lista de capas. Cuando crea un marco, las dimensiones iniciales vienen determinadas por su contenido. Los límites de su marco, por otro lado, son independientes de lo que haya dentro.

Su marco es similar a una ventana o, si lo prefiere, a una mesa de trabajo a través de la cual puede ver los objetos que hay detrás. Cuando redimensiona su marco, sólo está redimensionando la ventana a través de la cual mira. Diseñar con marcos es la clave para desbloquear las funciones más potentes de Figma. Podrá crear diseños bien organizados, con un bonito estilo, sencillos de utilizar, desplazables y redimensionables.

### **8.1 Tamaño individual**

El tamaño de un marco es independiente de sus hijos, las capas anidadas. ==El tamaño del marco padre no cambiará si se mueven o redimensionan los hijos==. Esto significa que el marco padre puede tener el mismo tamaño o ser mayor que sus hijos. Esto le permite hacer cosas como añadir relleno interno, crear un efecto de "máscara" y permitir la interacción de desplazamiento en un prototipo (ejemplos de ello a continuación). En contraste con los Grupos, en los que el grupo debe tener el mismo tamaño que sus hijos.

### **8.2 Utilizar estilos**

Los marcos, al igual que los rectángulos, son objetos a los que se les puede aplicar estilos. ==Pueden decorarse con un relleno, un trazo o una sombra. También pueden tener esquinas redondeadas==. Con este nivel de adaptabilidad, los marcos pueden utilizarse para diseñar casi cualquier cosa. Un botón, por ejemplo, puede crearse utilizando sólo un marco con estilo (azul con esquinas redondeadas) y una única capa de texto, a diferencia de los grupos, en los que se requiere una segunda capa para el fondo (lo que imposibilita el autodiseño).

### **8.3 Contenido desbordante**

Los hijos de un marco (capas anidadas) pueden "*desbordarse*" más allá de sus límites. Con la ayuda de "Recortar contenido", esos hijos fuera de los límites pueden mantenerse visibles u ocultos.

### **8.4 Redimensionamiento con restricciones**

Los hijos de un marco pueden aplicarse a restricciones de redimensionamiento (capas anidadas). Se utilizan para "constreñir" o "fijar" los hijos a la parte superior, inferior, central, izquierda o derecha del marco o para escalar a medida que cambia el tamaño.

### **8.5 Redimensionamiento automático**

La disposición automática puede aplicarse a los marcos para crear una variedad de comportamientos (automáticos) de redimensionamiento. La dirección en la que crecerá un marco, el espaciado entre los hijos (capas anidadas), el relleno interno y cómo responderá cada hijo individual a los cambios están todos determinados por la disposición automática. Se trata de una función muy potente que puede utilizarse de diversas maneras.

### **8.6 Disposiciones y cuadrículas**

Las cuadrículas y los diseños pueden aplicarse a cualquier marco, desde una gran "*mesa de trabajo*" del dispositivo hasta una región de la interfaz de usuario o un pequeño componente. Estos distintos marcos pueden incluso anidarse dentro de otro marco padre. Cuando se utiliza con restricciones, esto resulta útil para mantener un espaciado coherente entre distintos tamaños de contenedor y configurar el comportamiento del redimensionamiento. Un marco de escritorio, por ejemplo, puede tener un diseño para su marco de página anidado y otro para su marco de navegación lateral anidado. Cada uno tiene su propio comportamiento de redimensionamiento.

### **8.7 Crear componentes**

Para crear un componente, todas las capas del mismo deben estar alojadas en un único marco. Sin embargo, si estos elementos están alojados en un grupo, Figma convertirá automáticamente el grupo en un marco cuando haga clic en "*crear componente*".

## **Reflexiones finales**
---
Leer sobre todas las funciones disponibles con los marcos es útil, ¡pero el aprendizaje práctico es aún mejor!