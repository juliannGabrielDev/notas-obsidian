---
Fecha: 2024-12-23
Categoría: Evaluar el sitio web de Little Lemon
tags:
  - front-end
  - curso-7
  - modulo-2
---
## **1 La importancia de los formularios**
---
Cualquiera que utilice una aplicación o un sitio web tiene un objetivo específico en mente. ==Con frecuencia, un **formulario** es lo único que se **interpone** entre el usuario y su objetivo==. Los formularios siguen siendo uno de los tipos esenciales de interacción con el usuario en la web y en las aplicaciones. Los formularios se consideran con frecuencia el último paso para alcanzar los objetivos. **Los usuarios deben poder completar los formularios de forma rápida y sencilla**. Examinemos en detalle el formulario de pago actual de Little Lemon, que demuestra algunos errores comunes en el diseño de formularios.

## **2 El diseño**
---
En primer lugar, los campos de texto en los que el usuario debe introducir los datos están en el centro y no alineados a la izquierda como en las mejores prácticas. El botón de pago no es aparente y no hay cesta ni información sobre lo que el usuario está comprando.
### **2.1 ¿Qué pasa con la longitud?**

#### 2.1.1 Incluya un indicador de progreso

Normalmente, ==pasar por caja es un proceso de varios pasos==. Esto significa que el cliente tendrá que pasar por varios pasos antes de completar su pedido. Para que este proceso sea utilizable, incluya un **indicador de progreso** que indique en qué punto del proceso de pago se encuentra el cliente y cuánto tiempo le queda para completarlo.

![Formulario de maqueta de Little Lemon](formulario-little-lemon.webp)

#### 2.1.2 Incluya sólo los campos vitales

Un número récord de compradores están investigando posibles compras en sus smartphones. Mientras tanto, la pregunta más importante es si esos usuarios están dispuestos a comprar en sus dispositivos móviles. Todo el mundo ha respondido a preguntas temidas, como "*¿Cómo nos conoció?*" Aunque pueden servir al vendedor, no hacen nada por el comprador.

**Si bien estas preguntas son molestas en un ordenador de sobremesa, pueden ser fatales en un móvil**. En su excelente libro **Web Forms: Filling in The Blanks**, Luke Wroblewski afirma:

"*Cualquier pregunta que haga a la gente en un formulario Web requiere que la analicen, formulen una respuesta y luego introduzcan su respuesta en el affordance que usted ha proporcionado en el formulario. Estar atento a cada pregunta que hace le permite eliminar preguntas que no son absolutamente necesarias o que se pueden hacer en un momento o lugar mejor o que se pueden deducir automáticamente. Y cuantas menos preguntas haga, más probabilidades tendrá de que la gente rellene sus formularios rápida y fácilmente*"

La caja de Little Lemon demuestra cómo una experiencia sencilla puede complicarse rápidamente. Las páginas muestran campos innecesarios como la inicial del segundo nombre, el teléfono de la tarde y el teléfono móvil, mientras que, separando los campos, el campo Dirección tiene tres líneas imponentes y una Ciudad (en lugar de una sola para un código postal), además de que se espera que el usuario vuelva a escribir su dirección de correo electrónico.

#### 2.1.3 Campos obligatorios y errores

Tras rellenar los campos del formulario y hacer clic en enviar, se recibe un mensaje de error que impide al usuario continuar: "El nombre debe tener al menos 4 caracteres" Hay dos cuestiones a tener en cuenta según la captura de pantalla:

El nombre no es un campo obligatorio porque carece de asterisco (`*`) para indicar que el campo del formulario requiere entrada. Utilizar un asterisco para indicar los campos obligatorios en los formularios, según Nielsen Norman Group, es una forma sencilla de mejorar la usabilidad. El campo del formulario **tiene un número mínimo de caracteres**. Pequeños detalles como éste tienen un impacto significativo en la experiencia del usuario final en el diseño centrado en el usuario. Existen al menos 220 nombres de tres caracteres. En cierto modo, esto es deshumanizante porque el sistema considera a alguien como irreal o inválido.

#### 2.1.4 Campos obligatorios: una solución

Un asterisco o el texto requerido indican que un campo del formulario es obligatorio. Compruebe que todos los campos obligatorios del formulario están marcados. Incluya comentarios para resaltar errores como campos obligatorios vacíos, correo electrónico no válido (por ejemplo, cuando al correo electrónico le falta el signo '@'), etc. ¿Por qué tenemos un límite?

### **2.2 Límites de caracteres**

Los límites de caracteres son un tipo de limitación técnica que debe sacarse a la luz durante la colaboración entre desarrolladores y diseñadores. Un sistema necesitaría límites de caracteres inferiores y superiores por dos razones: **seguridad** y **almacenamiento**.

Debería realizarse una validación de la entrada para garantizar que es del tipo, longitud, formato y rango correctos. Como resultado, cuando los usuarios se registran para acceder a la información, ésta puede ser validada contra la base de datos. Una vulnerabilidad que permita a los usuarios introducir campos libremente daría lugar a datos inexactos y a la posibilidad de que los robots se introduzcan en su sistema.

Los límites máximos de caracteres se utilizan en el almacenamiento porque es imposible almacenar un nombre que tenga una longitud legítima de 1.073.741.823 bytes. El nombre más largo del mundo sólo tiene 747 caracteres.

#### 2.2.1 Límites de caracteres: una solución

Elimine el requisito del número mínimo de caracteres. Implemente un requisito de caracteres máximos que funcione para la gran mayoría de nombres de la base de datos: 50 caracteres es un excelente punto de partida. ¿Por qué tener un límite? ==Los límites de caracteres son un tipo de limitación técnica que *debería* ponerse de manifiesto durante la colaboración entre desarrolladores y diseñadores==. Un sistema requeriría límites de caracteres inferiores y superiores por motivos de seguridad y almacenamiento.

Debería realizarse una validación de la entrada para garantizar que es del tipo, longitud, formato y rango correctos. Como resultado, cuando los usuarios se registran para acceder a la información, ésta puede ser validada contra la base de datos. ==Una vulnerabilidad que permita a los usuarios introducir campos libremente daría lugar a datos desordenados y a la posibilidad de que los robots irrumpan en su sistema==.

### **2.3 Correo electrónico**

El usuario sólo va a pedir una comida, ¿necesita confirmar su correo electrónico? Si es importante, ==tenga en cuenta que cuando los usuarios están confirmando su correo electrónico en campos separados, suelen cometer errores tipográficos==. El requisito de que los usuarios escriban su correo electrónico en dos campos de texto aumenta la probabilidad de que se cometan errores tipográficos.

#### 2.3.1 Confirmación del correo electrónico: una solución

Así pues, el mejor enfoque sería enviar un enlace de confirmación al usuario. Este es el enfoque más fácil de utilizar porque requiere el menor esfuerzo por parte del usuario.

### **2.4 Pago sin explicar el CVV**

Al igual que AVS, CVV o CVC es un acrónimo ambiguo. Asegúrese de explicarlo.

#### 2.4.1 CVV: una solución

La imagen siguiente muestra que el CVV se encuentra en el reverso de su tarjeta bancaria y son los tres últimos dígitos impresos.

![Ilustración de una tarjeta de crédito con su valor de verificación compuesto de tres dígitos](cvv.webp)

## **Reflexiones finales**
---
Uno de los aspectos más frustrantes del uso de Internet es la validación de formularios. Si a un usuario no le queda claro qué está haciendo mal y no hay una forma fácil de solucionarlo, es mucho más probable que desista y se vaya a otro sitio cuando rellene un formulario.