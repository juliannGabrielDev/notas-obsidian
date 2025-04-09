---
Fecha: 2024-12-21
Categoría: Uso de activos en React
tags:
  - front-end
  - curso-5
  - modulo-3
---
## **Tarea**
---
Supongamos que está trabajando en un sitio web que permite a los visitantes reproducir sonidos de pájaros pulsando botones. La interfaz de usuario está configurada para que cuando un usuario pulse el botón,comience a reproducir el sonido del pájaro. Alternativamente, si el sonido del pájaro ya se está reproduciendo, al pausar el botón se pasará. Si se vuelve a pulsar el botón, el sonido seguirá reproduciéndose desde el punto en que se detuvo.

Aquí está el archivo **App.js** completado:

```jsx
import React from "react"; 
 
function App() { 
 
  const bird1 = new Audio( 
    "https://upload.wikimedia.org/wikipedia/commons/9/9b/Hydroprogne_caspia_-_Caspian_Tern_XC432679.mp3" 
  ); 
 
  const bird2 = new Audio( 
    "https://upload.wikimedia.org/wikipedia/commons/b/b5/Hydroprogne_caspia_-_Caspian_Tern_XC432881.mp3" 
  ); 
 
  function toggle1() { 
    if (bird1.paused) { 
      bird1.play(); 
    } else { 
      bird1.pause(); 
    } 
  }; 
 
  function toggle2() { 
    if (bird2.paused) { 
      bird2.play(); 
    } else { 
      bird2.pause(); 
    } 
  }; 
 
  return ( 
    <div> 
      <button onClick={toggle1}>Caspian Tern 1</button> 
      <button onClick={toggle2}>Caspian Tern 2</button> 
    </div> 
  ); 
} 
 
export default App;
```