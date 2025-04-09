---
Fecha: 2024-12-23
Categoría: Metodologías de evaluación
tags:
  - front-end
  - curso-7
  - modulo-2
---
La **accesibilidad** permite a las personas con discapacidad **interpretar**, **comprender**, **navegar**, **interactuar** y **contribuir** a la web. Piense en un mundo en el que los desarrolladores sepan todo lo que hay que saber sobre accesibilidad. Usted lo diseña y ellos lo construyen a la perfección. Sin embargo, si sólo tiene en cuenta el diseño de un producto, puede dificultar su uso a las personas con discapacidad.

Elegir para qué "*necesidades*" diseñar es uno de los problemas más comunes cuando se diseña para la accesibilidad. No excluimos intencionadamente a los usuarios, sino que 'no sabemos lo que no sabemos'. Como resultado, hay mucho que aprender sobre la accesibilidad. Consideremos algunas pautas de accesibilidad que pueden guiarle en la dirección correcta. Estas pautas cubren los puntos principales que debe conocer para que sus productos estén listos para el diseño y cumplan las normas mínimas de **la Sección 508 y las Pautas de Accesibilidad al Contenido en la Web (WCAG) 2.0**. El resto depende del desarrollo y de las pruebas de control de calidad. Si desea una explicación detallada de la accesibilidad, puede acceder a las [WCAG](https://www.w3.org/TR/WCAG20/) 2.0.

## **1 El acceso a la información no es un obstáculo para la innovación**
---
Es posible que la accesibilidad no le convenza para producir un producto feo, aburrido o desordenado. Puede que inicie una serie de limitaciones que deberá tener en cuenta a la hora de diseñar. Estas limitaciones de diseño le ofrecerán nuevas ideas que explorar, lo que se traducirá en productos mejorados para todos sus usuarios.

Tenga en cuenta que es posible que no quiera diseñar para sus compañeros mientras lee estas directrices. Lo importante es que diseñe para una amplia gama de usuarios que se relacionarán con sus productos, incluidas las personas ciegas, daltónicas o con mala visión, las sordas o con mala audición, las personas con problemas de movilidad permanentes o temporales y las personas con discapacidades cognitivas. Cuando diseñe, es conveniente que tenga en cuenta a todos los posibles usuarios. Pueden ser jóvenes, mayores, usuarios avanzados, usuarios ocasionales y aquellos que simplemente disfrutan de una buena experiencia.

## **2 No utilice sólo el color para transmitir información**
---
No utilice sólo el color para transmitir información. Esto puede ser útil para los usuarios que no pueden o tienen dificultades para distinguir un color de otro. Se incluyen las personas daltónicas (1 de cada 12 hombres y 1 de cada 200 mujeres), con baja visión (1 de cada 30 personas) o ciegas (1 de cada 188 personas).

Aunque el color puede utilizarse para transmitir información, no debe ser la única forma de hacerlo. Cuando utilice el color para distinguir elementos, puede ser útil proporcionar una identificación adicional que no dependa de la percepción del color. Para indicar los campos obligatorios de un formulario, puede utilizar un asterisco además del color y etiquetas para diferenciar zonas en los gráficos.

## **3 Proporcione un contraste suficiente entre el primer plano y el fondo**
---
El contraste entre los colores de primer plano y de fondo debe ser suficiente. Esto incluye el texto sobre imágenes, fondos degradados, botones y otros elementos. Esto no se aplica a los logotipos ni al texto incidental, como el que se encuentra en una fotografía. En las **Directrices de Accesibilidad al Contenido en la Web** se recomienda una relación de contraste entre el texto y el fondo de al menos 4,5 a 1. El mínimo desciende a 3 a 1 si su fuente tiene al menos 24 píxeles o 19 píxeles de negrita.

## **4 Asegúrese de que los elementos interactivos sean fácilmente identificables**
---
Para que los elementos interactivos, como **enlaces** y **botones**, sean más fáciles de identificar, ==considere la posibilidad de utilizar estilos distintos==. Para ello, por ejemplo, cambie el aspecto de los enlaces al pasar el ratón por encima, al enfocar con el teclado y al activarlos con la pantalla táctil. ==Asegúrese de que los estilos y la nomenclatura de los elementos interactivos sean coherentes en todo el sitio web==. Es posible que algunos usuarios no puedan utilizar el ratón y confíen únicamente en el teclado para navegar por las páginas web. Es fundamental que los usuarios puedan utilizar el teclado para acceder a todos los elementos interactivos y que quede claro qué elemento es interactivo. Se podría utilizar un borde o un resalte que se mueva a medida que se avanza por la página web para indicar el foco visible del teclado.

![Estilos únicos para diferentes tipos de enlaces](4-estilos-enlace.webp)

## **5 Asegúrese de que los elementos del formulario incluyen etiquetas claramente asociadas**
---
Es importante que cada campo tenga una etiqueta descriptiva, excepto las casillas de verificación y los botones de radio. Las casillas de verificación suelen colocarse a la derecha, y las etiquetas, de izquierda a derecha. Los idiomas se colocan a la izquierda o encima del área. Siempre es bueno comprobar que no haya demasiado espacio entre las etiquetas y los campos.

![El ejemplo del espacio destaca la relación entre los contenidos](5-etiquetas-formulario.webp)

## **6 Haga que las opciones de navegación sean claras y coherentes**
---
La navegación entre las páginas de un sitio web debe ser **coherente** en cuanto a **denominación**, **estilo** y **posicionamiento**. Una buena táctica es proporcionar más de una forma de navegar por sus páginas web, como una búsqueda en el sitio o un mapa del sitio. También puede utilizar pistas de orientación, como migas de pan y encabezados claros, para ayudar a los usuarios a comprender en qué parte de un sitio web o de una página se encuentran.

## **7 Proporcione retroalimentación fácilmente identificable**
---
La retroalimentación para interacciones como la confirmación de envío de formularios y la notificación al usuario cuando algo va mal pueden ser muy valiosas. Si hay instrucciones, deben ser claras. Los comentarios importantes que incluyan una acción del usuario deben mostrarse en un lugar donde puedan verse fácilmente.

![Ejemplo de lista de errores, icono y color de fondo para resaltar los errores](7-retroalimentacion.webp)

## **8 Utilice encabezamientos y espaciado para agrupar contenidos relacionados**
---
Los espacios en blanco y la proximidad ayudan a resaltar las relaciones entre los contenidos. Los encabezados pueden ayudarle a organizar el contenido, disminuir el desorden y hacer que sea más sencillo de escanear y comprender.

![Ejemplo de espaciado que resalta la relación entre los contenidos](8-espaciado.webp)

## **9 Diseñe para distintos tamaños de ventana gráfica**
---
Piense en cómo se visualiza la información de la página en distintos tamaños de ventana gráfica, como los teléfonos móviles o las ventanas del navegador ampliadas. La colocación y el aspecto de los elementos principales, como el encabezado y la navegación, pueden modificarse para aprovechar al máximo el espacio. Es útil comprobar que el tamaño del texto y el ancho de línea están ajustados para maximizar la legibilidad y la facilidad de lectura.

## **10 Proporcione controles para los contenidos que se inician automáticamente**
---
Puede permitir que los usuarios detengan cualquier animación o sonido de reproducción automática con controles visibles. Esto es válido para carruseles, deslizadores de imágenes, música de fondo y vídeos.

## **Reflexiones finales**
---
Cuanto más sensible sea a las necesidades de sus usuarios, más accesible será su diseño. Debe tener en cuenta a los usuarios de su grupo demográfico objetivo, a los usuarios de fuera de su grupo demográfico objetivo, a los usuarios con discapacidades e incluso a los usuarios de diferentes culturas y países. Una vez que conozca a fondo las necesidades de sus usuarios, podrá ayudarle a crear experiencias más accesibles para ellos.