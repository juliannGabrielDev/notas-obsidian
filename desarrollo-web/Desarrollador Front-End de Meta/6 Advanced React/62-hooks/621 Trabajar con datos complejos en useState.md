---
Fecha: 2024-12-30
Categoría: Introducción a los Hooks
tags:
  - front-end
  - curso-6
  - modulo-2
---
- [[#1 Un ejemplo de mantener el estado en un objeto y actualizarlo basándose en eventos generados por el usuario|1 Un ejemplo de mantener el estado en un objeto y actualizarlo basándose en eventos generados por el usuario]]
- [[#2 La forma correcta de actualizar el objeto de estado en React cuando se utiliza useState|2 La forma correcta de actualizar el objeto de estado en React cuando se utiliza useState]]
- [[#3 Formas incorrectas de intentar actualizar el objeto de estado|3 Formas incorrectas de intentar actualizar el objeto de estado]]
- [[#4 Actualizar el objeto de estado utilizando funciones de flecha|4 Actualizar el objeto de estado utilizando funciones de flecha]]
- [[#Conclusión|Conclusión]]

En esta lectura, aprenderá a utilizar objetos como variables de estado cuando utilice useState. También descubrirá la forma correcta de actualizar únicamente propiedades específicas, como los objetos de estado y por qué se hace esto. Esto se demostrará explorando lo que ocurre al cambiar el tipo de datos cadena por un objeto.

## 1 Un ejemplo de mantener el estado en un objeto y actualizarlo basándose en eventos generados por el usuario
---
Cuando necesite mantener el estado en un objeto y actualizarlo, inicialmente, podría intentar algo como esto:
```jsx
import { useState } from "react"; 
 
export default function App() { 
  const [greeting, setGreeting] = useState({ greet: "Hello, World" }); 
  console.log(greeting, setGreeting); 
 
  function updateGreeting() { 
    setGreeting({ greet: "Hello, World-Wide Web" }); 
  } 
 
  return ( 
    <div> 
      <h1>{greeting.greet}</h1> 
      <button onClick={updateGreeting}>Update greeting</button> 
    </div> 
  ); 
} 
```

Aunque esto funciona, **no es la forma recomendada de trabajar con objetos** de estado en React, esto se debe a que el objeto de estado suele tener más de una sola propiedad, y **es costoso actualizar todo el objeto sólo por actualizar una pequeña parte de él**.

## 2 La forma correcta de actualizar el objeto de estado en React cuando se utiliza useState
---
El enfoque sugerido para actualizar el objeto de estado en React cuando se utiliza useState es copiar el objeto de estado y luego actualizar la copia.

Esto suele implicar el uso del operador de propagación (`...`).

Teniendo esto en cuenta, aquí está el código actualizado:

```jsx
import { useState } from "react"; 
 
export default function App() { 
  const [greeting, setGreeting] = useState({ greet: "Hello, World" }); 
  console.log(greeting, setGreeting); 
 
  function updateGreeting() { 
    const newGreeting = {...greeting}; 
    newGreeting.greet = "Hello, World-Wide Web"; 
    setGreeting(newGreeting); 
  } 
 
  return ( 
    <div> 
      <h1>{greeting.greet}</h1> 
      <button onClick={updateGreeting}>Update greeting</button> 
    </div> 
  ); 
} 
```

## 3 Formas incorrectas de intentar actualizar el objeto de estado
---
Para demostrar que se necesita una copia del objeto de estado antiguo para actualizar el estado, exploremos lo que ocurre cuando se intenta actualizar el objeto de estado antiguo directamente:

```jsx
import { useState } from "react"; 
 
export default function App() { 
  const [greeting, setGreeting] = useState({ greet: "Hello, World" }); 
  console.log(greeting, setGreeting); 
 
  function updateGreeting() { 
    greeting = {greet: "Hello, World-Wide Web}; 
    setGreeting(greeting); 
  } 
 
  return ( 
    <div> 
      <h1>{greeting.greet}</h1> 
      <button onClick={updateGreeting}>Update greeting</button> 
    </div> 
  ); 
} 
```

El código anterior no funciona porque tiene un **TypeError** escondido en su interior.

Concretamente, el TypeError es: "Asignación a variable constante".

En otras palabras, no puede reasignar una variable declarada mediante const, como en el caso de la desestructuración de arrays del gancho useState:

```jsx
const [greeting, setGreeting] = useState({ greet: "Hello, World" }); 
```

Otro enfoque que podría intentar utilizar para sortear la forma sugerida de actualizar el estado cuando se trabaja con un objeto de estado podría ser el siguiente:

```jsx
import { useState } from "react"; 
 
export default function App() { 
  const [greeting, setGreeting] = useState({ greet: "Hello, World" }); 
  console.log(greeting, setGreeting); 
 
  function updateGreeting() { 
    greeting.greet = "Hello, World-Wide Web; 
    setGreeting(greeting); 
  } 
 
  return ( 
    <div> 
      <h1>{greeting.greet}</h1> 
      <button onClick={updateGreeting}>Update greeting</button> 
    </div> 
  ); 
} 
```

El código anterior es problemático porque no lanza ningún error; sin embargo, tampoco actualiza el encabezado, por lo que no está funcionando correctamente. Esto significa que, independientemente de cuántas veces haga clic en el botón "Actualizar saludo", éste seguirá siendo "Hola, mundo".

Para reiterar, la forma correcta de trabajar con el estado cuando se guarda como un objeto es

1. Copiar el antiguo objeto de estado utilizando el operador spread (...) y guardarlo en una nueva variable y
2. Pasar la nueva variable a la función de actualización del estado.

## 4 Actualizar el objeto de estado utilizando funciones de flecha
---
Utilicemos ahora un objeto más complejo para actualizar el estado.

El objeto de estado tiene ahora dos propiedades: saludo y ubicación.

La intención de esta actualización es demostrar qué hacer cuando sólo cambia una propiedad específica del objeto de estado, manteniendo el resto de propiedades sin cambios:

```jsx
import { useState } from "react"; 
 
export default function App() { 
  const [greeting, setGreeting] = useState( 
    { 
        greet: "Hello", 
        place: "World" 
    } 
  ); 
  console.log(greeting, setGreeting); 
 
  function updateGreeting() { 
    setGreeting(prevState => { 
        return {...prevState, place: "World-Wide Web"} 
    }); 
  } 
 
  return ( 
    <div> 
      <h1>{greeting.greet}, {greeting.place}</h1> 
      <button onClick={updateGreeting}>Update greeting</button> 
    </div> 
  ); 
} 
```

La razón por la que esto funciona es porque utiliza el estado anterior, que se llama prevState, y éste es el valor anterior de la variable saludo. En otras palabras, hace una copia del objeto prevState, y actualiza sólo la propiedad place del objeto copiado. A continuación, devuelve un objeto nuevo:

```jsx
return {...prevState, place: "World-Wide Web"} 
```

Todo se envuelve entre llaves para que este nuevo objeto se construya correctamente, y se devuelve desde la llamada a `setGreeting`.

## Conclusión
---
Ha aprendido lo que ocurre al cambiar el tipo de datos cadena a un objeto, con ejemplos de cómo mantener el estado en un objeto y actualizarlo en función de eventos generados por el usuario. También ha aprendido sobre las formas correctas e incorrectas de actualizar el objeto de estado en React cuando se utiliza useState, y sobre la actualización del objeto de estado utilizando funciones de flecha.

```button
name Índice del Curso 6
type link
action obsidian://open?vault=markdown-notes&file=desarrollo-web%2F6%20Advanced%20React%2F%C3%8Dndice%20del%20curso%206
customColor #10b981
customTextColor #ecfdf5
```