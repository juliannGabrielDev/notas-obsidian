---
Fecha: 2024-12-31
Categoría: Reglas de los hooks y obtención de datos con hooks
tags:
  - front-end
  - curso-6
  - modulo-2
---
Ha aprendido más sobre la obtención de datos mediante hooks y que la obtención de datos de una API de terceros se considera un efecto secundario que requiere el uso del gancho `useEffect` para tratar las llamadas a la API Fetch en React.

También ha explorado cómo la respuesta de la obtención de datos de terceros puede fallar, o retrasarse, y que puede ser útil proporcionar diferentes renders, en función de si los datos se han recibido o no.

En esta lectura, explorará los diferentes enfoques para configurar el gancho `useEffect` al obtener datos JSON de la web. También aprenderá por qué puede ser útil proporcionar diferentes renders, en función de si los datos se han recibido o no.

Anteriormente ha aprendido a utilizar la API Fetch para obtener algunos datos JSON de un sitio web de terceros en JavaScript plano.

Le alegrará saber que la obtención de datos no es tan diferente en React.

Sólo hay un ingrediente más que debe tener en cuenta al trabajar con React, a saber, que la obtención de datos de una API de terceros se considera un efecto secundario.

Al ser un efecto secundario, necesita utilizar el gancho `useEffect` para tratar con el uso de las llamadas a la API Fetch en React.

Para entender lo que esto implica, permítame ilustrarlo con un ejemplo de código en el que un componente está obteniendo algunos datos de una API externa para mostrar información sobre una criptomoneda.

```jsx
import { useState, useEffect } from "react"; 
 
export default function App() { 
  const [btcData, setBtcData] = useState({}); 
  useEffect(() => { 
    fetch(`https://api.coindesk.com/v1/bpi/currentprice.json`) 
      .then((response) => response.json()) 
      .then((jsonData) => setBtcData(jsonData.bpi.USD)) 
      .catch((error) => console.log(error)); 
  }, []); 
 
  return ( 
    <> 
      <h1>Current BTC/USD data</h1> 
      <p>Code: {btcData.code}</p> 
      <p>Symbol: {btcData.symbol}</p> 
      <p>Rate: {btcData.rate}</p> 
      <p>Description: {btcData.description}</p> 
      <p>Rate Float: {btcData.rate_float}</p> 
    </> 
  ); 
} 
```

Este ejemplo muestra que para obtener datos de una API de terceros, es necesario pasar una función anónima como llamada al gancho `useEffect`.

```jsx
useEffect( 
    () => { 
        // ... data fetching code goes here 
    }, 
    [] 
); 
```

El código anterior enfatiza el hecho de que el gancho `useEffect` toma dos argumentos, y que el primer argumento contiene la función anónima que, dentro de su cuerpo, contiene el código de obtención de datos.

Alternativamente, podría extraer esta función anónima en una expresión de función separada o declaración de función, y luego simplemente hacer referencia a ella.

Utilizando el ejemplo anterior, ese código podría presentarse como sigue:

```jsx
import { useState, useEffect } from "react"; 
 
export default function App() { 
  const [btcData, setBtcData] = useState({}); 
 
  const fetchData = () => { 
    fetch(`https://api.coindesk.com/v1/bpi/currentprice.json`) 
      .then((response) => response.json()) 
      .then((jsonData) => setBtcData(jsonData.bpi.USD)) 
      .catch((error) => console.log(error)); 
  }; 
 
  useEffect(() => { 
    fetchData(); 
  }, []); 
 
  return ( 
    <> 
      <h1>Current BTC/USD data</h1> 
      <p>Code: {btcData.code}</p> 
      <p>Symbol: {btcData.symbol}</p> 
      <p>Rate: {btcData.rate}</p> 
      <p>Description: {btcData.description}</p> 
      <p>Rate Float: {btcData.rate_float}</p> 
    </> 
  ); 
} 
```

El código hace esencialmente lo mismo, pero este segundo ejemplo es más limpio y está mejor organizado.

Una cosa adicional que puede discutirse aquí es la declaración return del ejemplo anterior.

Muy a menudo, la respuesta de la obtención de datos de terceros puede fallar, o retrasarse. Por eso puede ser útil proporcionar diferentes renders, en función de si los datos se han recibido o no.

El renderizado condicional más sencillo podría consistir en configurar dos renders, en función de si los datos se han obtenido con éxito o no.

Por ejemplo:

```jsx
 return someStateVariable.length > 0 ? ( 
    <div> 
      <h1>Data returned:</h1> 
      <h2>{someStateVariable.results[0].price}</h2> 
    </div> 
  ) : ( 
    <h1>Data pending...</h1> 
  ); 
```

En este ejemplo, devuelvo condicionalmente un h1 y un h2, **si** la longitud del enlace `someStateVariable` es superior a 0.

Este enfoque funcionaría si el `someStateVariable` contiene una matriz.

Si el `someStateVariable` se inicializa como un array vacío, pasado a la llamada al gancho `useState`, entonces sería posible actualizar esta variable de estado con un elemento del array que podría ser devuelto desde una llamada `fetch()` a un proveedor de datos JSON de terceros.

Si esto funciona como se ha descrito anteriormente, la longitud del `someStateVariable` aumentaría desde la longitud inicial de cero - porque la longitud de un array vacío es cero.

Inspeccionemos de nuevo la condicional `return`:

```jsx
 return someStateVariable.length > 0 ? ( 
    <div> 
      <h1>Data returned:</h1> 
      <h2>{someStateVariable.results[0].price}</h2> 
    </div> 
  ) : ( 
    <h1>Data pending...</h1> 
  ); 
```

Si la obtención de datos falla, aparecerá en pantalla el texto `"Data pending..."`, ya que la longitud del `someStateVariable` seguirá siendo cero.

## Conclusión
---
Ha aprendido más sobre la obtención de datos mediante ganchos y que la obtención de datos de una API de terceros se considera un efecto secundario que requiere el uso del gancho `useEffect` para tratar las llamadas a la API Fetch en React.

También ha explorado cómo la respuesta de la obtención de datos de terceros puede fallar, o retrasarse, y que puede ser útil proporcionar diferentes renders, en función de si los datos se han recibido o no.

```button
name Índice del Curso 6
type link
action obsidian://open?vault=markdown-notes&file=desarrollo-web%2F6%20Advanced%20React%2F%C3%8Dndice%20del%20curso%206
customColor #10b981
customTextColor #ecfdf5
```