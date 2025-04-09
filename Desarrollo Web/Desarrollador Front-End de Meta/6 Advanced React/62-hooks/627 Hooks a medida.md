---
Fecha: 2024-12-31
Categoría: Hooks avanzados
tags:
  - front-end
  - curso-6
  - modulo-2
---
- [[#1 Cómo nombrar un hook personalizado|1 Cómo nombrar un hook personalizado]]
	- [[#1 Cómo nombrar un hook personalizado#1.1 Codificación de un hook personalizado|1.1 Codificación de un hook personalizado]]
	- [[#1 Cómo nombrar un hook personalizado#1.2 Uso de un hook personalizado|1.2 Uso de un hook personalizado]]
- [[#Conclusión|Conclusión]]

React tiene algunos hooks incorporados, como el hook `useState`, o el hook `useRef`, sobre los que ya ha aprendido antes. Sin embargo, como desarrollador de React, puede escribir sus propios hooks. Entonces, ¿por qué querría escribir un hook personalizado?

En esencia, ==los hooks le proporcionan una forma repetible y racionalizada de tratar requisitos específicos en sus aplicaciones React==. Por ejemplo, el hook `useState` nos proporciona una forma fiable de tratar las actualizaciones de estado en los componentes React.

==Un **hook personalizado** es simplemente una manera de extraer una pieza de funcionalidad que puede utilizar una y otra vez==. Dicho de otra manera, puede codificar un hook personalizado cuando quiera evitar la duplicación o cuando no quiera construir una pieza de funcionalidad desde cero a través de múltiples proyectos React. Al codificar un hook personalizado, puede crear una forma fiable y ágil de reutilizar una pieza de funcionalidad en sus aplicaciones React.

Para entender cómo funciona esto, vamos a explorar cómo construir un hook personalizado. Para poner esto en contexto, también vamos a codificar una aplicación React muy simple.

Toda la aplicación React se encuentra dentro del componente **App** de abajo:

```jsx
import { useState } from "react"; 
 
function App() { 
  const [count, setCount] = useState(0); 
 
  function increment() { 
    setCount(prevCount => prevCount + 1) 
  } 
 
  return ( 
    <div> 
      <h1>Count: {count}</h1> 
      <button onClick={increment}>Plus 1</button> 
    </div> 
  ); 
} 
 
export default App; 
```

Se trata de una app sencilla con un encabezado `h1` que muestra el valor de la variable de estado recuento y un botón con un atributo de gestión de eventos `onClick` que, cuando se dispara, invoca la función `increment()`.

El hook también será sencillo. Registrará por consola el valor de una variable cada vez que se actualice.

Recuerde que la forma correcta de manejar las invocaciones de `console.log()` es utilizar el gancho `useEffect`.

Por lo tanto, esto significa que mi hook personalizado

1. Necesitará utilizar el gancho useEffect y
2. Ser un archivo separado que luego utilizará en el componente App.

## 1 Cómo nombrar un hook personalizado
---
Un hook personalizado necesita tener un nombre que empiece por `use`.

Dado que el hook de este ejemplo se utilizará para registrar valores en la consola, vamos a nombrar el gancho `useConsoleLog`.

### 1.1 Codificación de un hook personalizado

Ahora es el momento de explorar cómo codificar el hook personalizado.

En primer lugar, lo añadiremos como un archivo independiente, que podemos llamar **useConsoleLog.js**, y lo añadiremos a la raíz de la carpeta src, en el mismo lugar donde se encuentra el componente **App.js**.

Aquí está el código del archivo **useConsoleLog.js**:

```jsx
import { useEffect } from "react";

function useConsoleLog(varName) {
  useEffect(() => {
    console.log(varName);
  }, [varName]);
}

export default useConsoleLog;
```

### 1.2 Uso de un hook personalizado

Ahora que el hook personalizado ha sido codificado, puede utilizarlo en cualquier componente de su app.

Dado que la app del ejemplo sólo tiene un único componente, llamado **App**, puede utilizarlo para actualizar este componente.

El hook `useConsoleLog` puede importarse de la siguiente manera:

```jsx
import useConsoleLog from "./useConsoleLog";
```

Y luego, para utilizarlo, bajo el código de establecimiento del estado, simplemente añadiré la siguiente línea de código:

```jsx
useConsoleLog(count);
```

Aquí está el código completo del archivo **App.js**:

```jsx
import { useState } from "react";
import useConsoleLog from "./useConsoleLog";

function App() {
  const [count, setCount] = useState(0);
  useConsoleLog(count);

  function increment() {
    setCount(prevCount => prevCount + 1);
  }

  return (
    <div>
      <h1>Count: {count}</h1>
      <button onClick={increment}>Plus 1</button>
    </div>
  );
}

export default App;
```

Esta actualización confirma la afirmación hecha al principio de esta lectura, y es que los hooks personalizados son una forma de extraer funcionalidad que luego puede ser reutilizada a lo largo de sus aplicaciones React.

## Conclusión
---
Usted ha aprendido cómo nombrar, construir y utilizar hooks personalizados en React.

```button
name Índice del Curso 6
type link
action obsidian://open?vault=markdown-notes&file=desarrollo-web%2F6%20Advanced%20React%2F%C3%8Dndice%20del%20curso%206
customColor #10b981
customTextColor #ecfdf5
```