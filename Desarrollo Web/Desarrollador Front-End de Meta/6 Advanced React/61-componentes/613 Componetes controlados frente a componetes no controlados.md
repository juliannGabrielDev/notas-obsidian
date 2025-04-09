---
Fecha: 2024-12-21
Categoría: Formularios en React
tags:
  - front-end
  - curso-6
  - modulo-1
---
Esta lectura le enseñará cómo trabajar con entradas no controladas en React y las ventajas de las entradas controladas mediante el diseño de estados. También aprenderá cuándo elegir entradas controladas o no controladas y las características que admite cada opción.

## **Introducción**
---
En la mayoría de los casos, React recomienda utilizar componentes controlados para implementar formularios. Aunque este enfoque se alinea con el modelo declarativo de React, los campos de formulario no controlados siguen siendo una opción válida y tienen su mérito. Vamos a desglosarlos para ver las diferencias entre los dos enfoques y cuándo debe utilizar cada método.

## **1 Entradas no controladas**
---
Las entradas no controladas son como las entradas de formulario HTML estándar:

```jsx
const Form = () => { 
 return ( 
   <div> 
     <input type="text" /> 
   </div> 
 ); 
}; 
```

Recuerdan exactamente lo que usted tecleó, siendo el propio DOM el que mantiene ese estado interno. ¿Cómo puede entonces obtener su valor? La respuesta es utilizando una referencia React.

En el código siguiente, puede ver cómo se utiliza una ref para acceder al valor de la entrada cada vez que se envía el formulario.

```jsx
const Form = () => { 
 const inputRef = useRef(null); 

 const handleSubmit = () => { 
   const inputValue = inputRef.current.value; 
   // Do something with the value 
 } 
 return ( 
   <form onSubmit={handleSubmit}> 
     <input ref={inputRef} type="text" /> 
   </form> 
 ); 
}; 
```

En otras palabras, debe **extraer** el valor del campo cuando sea necesario.

Los componentes no controlados son la forma más sencilla de implementar entradas de formulario. Sin duda hay casos valiosos para ellos, especialmente cuando su formulario es sencillo. Por desgracia, no son tan potentes como sus homólogos, así que veamos a continuación las entradas controladas.

## **2 Entradas controladas**
---
Las entradas controladas aceptan su valor actual como prop y una llamada de retorno para cambiar ese valor. Eso implica que el valor de la entrada tiene que vivir en el estado de React en alguna parte. Típicamente, el componente que renderiza el input (como un componente de formulario) guarda eso en su estado:

```jsx
const Form = () => { 
 const [value, setValue] = useState(""); 

 const handleChange = (e) => { 
   setValue(e.target.value) 
 } 

 return ( 
   <form> 
     <input 
       value={value} 
       onChange={handleChange} 
       type="text" 
     /> 
   </form> 
 ); 
}; 
```

Cada vez que se teclea un nuevo carácter, se ejecuta la función `handleChange`. Recibe el nuevo valor de la entrada, y luego lo establece en el estado. En el ejemplo de código anterior, el flujo sería el siguiente:

- La entrada comienza con una cadena vacía: `“”`

- Usted teclea “a” y `handleChange` obtiene un “a” adjunto en el objeto de evento, como `e.target.value`, y posteriormente llama a `setValue` con él. La entrada se actualiza entonces para tener el valor de “a”.

- Usted teclea “b” y `handleChange` es llamado con `e.target.value` siendo “ab”.y establece eso en el estado. Eso se establece en el estado. A continuación, la entrada se vuelve a renderizar una vez más, ahora con `value = "ab"`.

Este flujo **empuja** los cambios de valor al componente formulario en lugar de tirar como en el ejemplo `ref` de la versión no controlada. Por lo tanto, el componente formulario siempre tiene el valor actual de la entrada sin necesidad de pedirlo explícitamente.

Como resultado, sus datos (estado React) y la interfaz de usuario (etiquetas de entrada) están siempre sincronizados. Otra implicación es que los formularios pueden responder a los cambios de entrada de forma inmediata, por ejemplo, mediante:

- Validación instantánea por campo

- Desactivando el botón de envío a menos que todos los campos tengan datos válidos

- Imponiendo un formato de entrada específico, como números de teléfono o de tarjeta de crédito

A veces se encontrará con que no necesita nada de eso. En ese caso, no controlado podría ser una opción más sencilla.

## **3 El tipo de entrada**
---
Hay algunas entradas de formulario específicas que siempre son incontroladas, como la etiqueta de entrada de archivo.

En React, un `<input type="file" />` es siempre un componente no controlado porque su valor es de sólo lectura y no puede establecerse mediante programación.

El siguiente ejemplo ilustra cómo crear una referencia al nodo DOM para acceder a cualquier archivo seleccionado en el manejador de envío del formulario:

```jsx
const Form = () => { 
 const fileInput = useRef(null); 

 const handleSubmit = (e) => { 
   e.preventDefault(); 
   const files = fileInput.current.files; 
   // Do something with the files here 
 } 

 return ( 
   <form onSubmit={handleSubmit}> 
     <input 
       ref={fileInput} 
       type="file" 
     /> 
   </form> 
 ); 
}; 
```

## **Conclusión**
---
Los componentes no controlados con refs están bien si su formulario es increíblemente simple en cuanto a la respuesta de la interfaz de usuario. Sin embargo, los campos de entrada controlados son el camino a seguir si necesita más funciones en sus formularios.

Evalúe su situación específica y elija la opción que más le convenga.

La tabla siguiente resume las características que admite cada una:

| Característica                                                | No controlado | Controlada |
| ------------------------------------------------------------- | ------------- | ---------- |
| Recuperación de valores una sola vez (por ejemplo, al enviar) | **Sí**        | **Sí**     |
| Validación al enviar                                          | **Sí**        | **Sí**     |
| Validación instantánea de campos                              | No            | **Sí**     |
| Desactivación condicional de un botón de envío                | No            | **Sí**     |
| Imponer un formato de entrada específico                      | No            | **Sí**     |
| Varias entradas para un dato                                  | No            | **Sí**     |
| Entradas dinámicas                                            | No            | **Sí**     |

Y eso es todo sobre los componentes controlados frente a los no controlados. Ha conocido en detalle cada opción, cuándo elegir una u otra y, por último, una comparación de las características admitidas.