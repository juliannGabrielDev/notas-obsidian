---
Fecha: 2024-12-30
Categoría: Introducción a los Hooks
tags:
  - front-end
  - curso-6
  - modulo-2
---
Se le ha presentado el uso principal del gancho `useEffect`, un gancho React incorporado muy adecuado para realizar efectos secundarios en sus componentes React.

En esta lectura se le presentará el uso correcto de la matriz de dependencias y las distintas llamadas a `useEffect` que pueden utilizarse para separar distintas preocupaciones. También aprenderá cómo puede limpiar recursos y liberar memoria en su lógica `useEffect` devolviendo una función.

El código que coloque dentro del gancho `useEffect` siempre se ejecuta después de que su componente se monte o, en otras palabras, después de que React haya actualizado el DOM.

Además, dependiendo de su configuración a través de la matriz de dependencias, sus efectos también pueden ejecutarse cuando cambien ciertas variables de estado o props.

Por defecto, si no se proporciona un segundo argumento a la función useEffect, el efecto se ejecutará después de cada renderización.

```jsx
useEffect(() => { 
   document.title = 'Little Lemon';
 }); 
```

Sin embargo, eso puede causar problemas de rendimiento, especialmente si sus efectos secundarios son computacionalmente intensivos. Una forma de indicar a React que omita la aplicación de un efecto es pasar una matriz como segundo parámetro a useEffect.

En el ejemplo siguiente, la variable entera `version` se pasa como segundo parámetro. Esto significa que el efecto sólo se volverá a ejecutar si el número `version` cambia entre renders.

```jsx
useEffect(() => { 
  document.title = `Little Lemon, v${version}`;
}, [version]); // Only re-run the effect if version changes 
```

Si `version` es 2 y el componente se vuelve a renderizar y la versión sigue siendo igual a 2, React comparará `[2]` de la renderización anterior y `[2]` de la siguiente. Como todos los elementos de la matriz son iguales, React omitiría la ejecución del efecto.

**Utilice múltiples efectos para separar preocupaciones**

React no le limita en el número de efectos que puede tener su componente. De hecho, le anima a agrupar la lógica relacionada en el mismo efecto y a dividir la lógica no relacionada en efectos diferentes.

```jsx
function MenuPage(props) { 
  const [data, setData] = useState([]); 

  useEffect(() => { 
    document.title = 'Little Lemon'; 
  }, []); 

  useEffect(() => { 
    fetch(`https://littlelemon/menu/${id}`) 
      .then(response => response.json()) 
      .then(json => setData(json)); 
  }, [props.id]); 

  // ... 
} 
```

Los ganchos múltiples le permiten dividir el código en función de lo que esté haciendo, mejorando la legibilidad del código y la modularidad.

## 1 Efectos con limpieza
---
Algunos efectos secundarios pueden necesitar limpiar recursos o memoria que ya no se necesitan, evitando así fugas de memoria que podrían ralentizar sus aplicaciones.

Por ejemplo, puede que desee configurar una suscripción a una fuente de datos externa. En ese escenario, es vital realizar una limpieza después de que el efecto termine su ejecución.

¿Cómo puede lograrlo? En línea con el punto anterior de dividir el código en función de lo que está haciendo, el gancho useEffect ha sido diseñado para mantener el código para añadir y eliminar una suscripción junto, ya que está estrechamente relacionado.

Si su efecto devuelve una función, React la ejecutará cuando llegue el momento de limpiar los recursos y liberar la memoria no utilizada.

```jsx
function LittleLemonChat(props) { 
  const [status, chatStatus] = useState('offline'); 

  useEffect(() => { 
    LemonChat.subscribeToMessages(props.chatId, () => setStatus('online')) 

    return () => { 
      setStatus('offline'); 
      LemonChat.unsubscribeFromMessages(props.chatId); 
    }; 
  }, []); 

  // ... 
} 
```

Devolver una función es opcional y es el mecanismo que React proporciona en caso de que necesite realizar una limpieza adicional en sus componentes.

React se asegurará de ejecutar la lógica de limpieza cuando sea necesario. La ejecución se producirá siempre cuando el componente se desmonte. Sin embargo, en los efectos que se ejecutan después de cada renderizado y no sólo una vez, React también limpiará el efecto del renderizado anterior antes de ejecutar el nuevo efecto la próxima vez.

## Conclusión
---
En esta lección, ha aprendido algunos consejos prácticos para utilizar el gancho incorporado Efecto. En particular, se le presentó cómo utilizar la matriz de dependencia correctamente, cómo separar diferentes preocupaciones en diferentes efectos y, por último, cómo limpiar los recursos no utilizados mediante la devolución de una función opcional dentro del efecto.

```button
name Índice del Curso 6
type link
action obsidian://open?vault=markdown-notes&file=desarrollo-web%2F6%20Advanced%20React%2F%C3%8Dndice%20del%20curso%206
customColor #10b981
customTextColor #ecfdf5
```