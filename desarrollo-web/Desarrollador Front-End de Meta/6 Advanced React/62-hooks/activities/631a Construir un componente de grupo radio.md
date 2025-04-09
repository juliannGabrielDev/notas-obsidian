---
Fecha: 2024-12-31
Categoría: Inmersión profunda en JSX
tags:
  - front-end
  - curso-6
  - actividades
---
Este código de React muestra un formulario con opciones de radio (botones redondos que permiten seleccionar una opción). Al seleccionar una opción, el botón de "Submit" se habilita.

---

### **`App.jsx` (Componente principal)**

```javascript
import { RadioGroup, RadioOption } from "./exercises/index";
import { useState } from "react";

function App() {
  const [selected, setSelected] = useState("");  // Estado para almacenar la opción seleccionada

  return (
    <div>
      <h2>How did you hear about Little Lemon?</h2>
      
      <RadioGroup onChange={setSelected} selected={selected}>
        <RadioOption value="social_media">Social Media</RadioOption>
        <RadioOption value="friends">Friends</RadioOption>
        <RadioOption value="advertising">Advertising</RadioOption>
        <RadioOption value="other">Other</RadioOption>
      </RadioGroup>
      
      <button disabled={!selected}>Submit</button>  // Botón que se desactiva si no hay opción seleccionada
    </div>
  );
}

export default App;
```

---

### Explicación del Componente `App`

- **`useState("")`** – Se usa para manejar el estado de la opción seleccionada. Inicia vacío (`""`).
- **`RadioGroup` y `RadioOption`** – Son componentes personalizados que manejan las opciones de radio.
- **`selected`** – Almacena qué opción de radio está seleccionada.
- **`setSelected`** – Es la función que actualiza ese estado.

Cuando seleccionas una opción:

1. **`onChange={setSelected}`** – Actualiza el estado `selected` con el valor de la opción elegida.
2. **`disabled={!selected}`** – El botón "Submit" solo se habilita si `selected` tiene un valor (es decir, si hay una opción elegida).

---

### **`index.jsx` (Definición de `RadioGroup` y `RadioOption`)**

```javascript
import * as React from "react";

export const RadioGroup = ({ onChange, selected, children }) => { 
  const RadioOptions = React.Children.map(children, (child) => { 
    return React.cloneElement(child, { 
      onChange, 
      checked: child.props.value === selected, 
    }); 
  }); 
  return <div className="RadioGroup">{RadioOptions}</div>; 
};
```

---

### Explicación de `RadioGroup`

- **`children`** – Es todo lo que `RadioGroup` tiene dentro (las `RadioOption`).
- **`React.Children.map`** – Recorre todos los `RadioOption` que están dentro de `RadioGroup`.
- **`React.cloneElement`** – Copia cada `RadioOption` y le pasa las props `onChange` y `checked`.
- **`checked: child.props.value === selected`** – Marca como `checked` (seleccionado) la opción cuyo valor coincida con el estado `selected`.

---

### **`RadioOption` (Botón individual)**

```javascript
export const RadioOption = ({ value, checked, onChange, children }) => { 
    return ( 
      <div className="RadioOption"> 
        <input 
          id={value} 
          type="radio" 
          name={value} 
          value={value} 
          checked={checked} 
          onChange={(e) => { 
            onChange(e.target.value); 
          }} 
        /> 
        <label htmlFor={value}>{children}</label> 
      </div> 
    ); 
};
```

---

### Explicación de `RadioOption`

- **`value`** – Es el valor único de cada opción (`social_media`, `friends`, etc.).
- **`checked`** – Indica si la opción está marcada.
- **`onChange`** – Llama a la función `setSelected` cuando cambia la opción.
- **`children`** – Es el texto que se muestra al lado del botón (ej. "Social Media").

Cuando haces clic en un botón:

1. **`onChange={(e) => { onChange(e.target.value); }}`** – Toma el valor (`value`) de la opción seleccionada y actualiza el estado.

---

### Flujo Completo 🚀

1. El componente `App` muestra el formulario con opciones de radio.
2. Cuando seleccionas una opción, `setSelected` guarda su valor.
3. El botón "Submit" se habilita porque `selected` ya no está vacío.

---

### Visualización:

```
How did you hear about Little Lemon?  
(•) Social Media  
( ) Friends  
( ) Advertising  
( ) Other  
[Submit]  
```