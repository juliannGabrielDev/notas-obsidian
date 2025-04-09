---
Fecha: 2024-12-31
Categoría: Hooks avanzados
tags:
  - front-end
  - curso-6
  - actividades
---
- [[#Tarea|Tarea]]
- [[#Concepto Clave: Cierre de JavaScript (Closures) y useEffect|Concepto Clave: Cierre de JavaScript (Closures) y useEffect]]
	- [[#Concepto Clave: Cierre de JavaScript (Closures) y useEffect#Analizando el Flujo|Analizando el Flujo]]

## Tarea
---
Ha aprendido a codificar un hook personalizado en React. En este laboratorio de código, practicará la escritura de un nuevo hook personalizado.

El código de inicio de esta aplicación contiene código que mostrará el día de la semana dentro de un encabezado `h1`, por ejemplo: `"Today is: Monday"`. También hay un botón debajo de este encabezado, que dice `"Get next day"`.

Cuando un usuario pulsa sobre este botón, el encabezamiento `h1` se actualiza para que el mensaje muestre el día siguiente en la secuencia.

Su tarea consiste en completar el gancho personalizado llamado `usePrevious` para que la cabecera `h1` muestre tanto el día actual como el día actual anterior antes de la actualización.

```jsx
import { useState, useEffect, useRef } from "react";
export default function App() {
  const [day, setDay] = useState("Monday");
  const prevDay = usePrevious(day);
  const getNextDay = () => {
    if (day === "Monday") {
      setDay("Tuesday")
    } else if (day === "Tuesday") {
      setDay("Wednesday")
    } else if (day === "Wednesday") {
      setDay("Thursday")
    } else if (day === "Thursday") {
      setDay("Friday")
    } else if (day === "Friday") {
      setDay("Monday")
    }
  }
  return (
    <div style={{padding: "40px"}}>
      <h1>
        Today is: {day}<br />
        {
          prevDay && (
            <span>Previous work day was: {prevDay}</span>
          )
        }
      </h1>
      <button onClick={getNextDay}>
        Get next day
      </button>
    </div>
  );
}
function usePrevious(val) {
  const ref = useRef();
  useEffect(() => {
    ref.current = val;
  }, [val]);
  return ref.current;
}
```

## Concepto Clave: Cierre de JavaScript (Closures) y useEffect

El truco está en cómo funciona `useEffect` y `useRef` en React.

Cuando el estado (`day`) cambia, React renderiza el componente desde cero, pero las referencias (`ref`) permanecen intactas entre renderizados. Esto es lo que permite guardar el valor anterior.

---

### Analizando el Flujo

Vamos a seguir el ciclo con un ejemplo práctico:

1. Renderizado inicial:

```jsx
const [day, setDay] = useState("Monday"); // day = "Monday"
const prevDay = usePrevious(day);  // prevDay es undefined inicialmente
```

El valor de `day` es `"Monday"`.

`usePrevious` se llama con `val = "Monday"`.

`ref.current` todavía no tiene valor.



---

2. Primer renderizado:

```jsx
useEffect(() => {
  ref.current = "Monday";  // Se guarda "Monday" en ref.current
}, ["Monday"]);
```

Después del renderizado, ref.current ahora es "Monday".

---

3. Clic en el botón (cambia a `"Tuesday"`):

```jsx
setDay("Tuesday");  // Cambia el estado a "Tuesday"
```

El componente se vuelve a renderizar con `day = "Tuesday"`.

`usePrevious("Tuesday")` se llama, pero `ref.current` aún tiene `"Monday"`.

---

4. Segundo renderizado:

```jsx
useEffect(() => {
  ref.current = "Tuesday";  // Ahora se guarda "Tuesday" en ref.current
}, ["Tuesday"]);
```

ANTES de que esto ocurra, `ref.current` devuelve `"Monday"` como el valor anterior (`prevDay`).

Después, `ref.current` se actualiza a `"Tuesday"`.

---

¿Por qué el valor anterior se guarda?

La clave es esta línea:

`return ref.current;`

Cuando `usePrevious` devuelve `ref.current`, lo hace antes de que `useEffect` actualice el valor.

**Por eso:**

- El valor anterior siempre está disponible en `ref.current` hasta que `useEffect` lo sobrescribe con el nuevo valor.

- Esto es posible gracias a que `useRef` no causa renderizados, simplemente guarda datos entre renderizados.

```button
name Índice del Curso 6
type link
action obsidian://open?vault=markdown-notes&file=desarrollo-web%2F6%20Advanced%20React%2F%C3%8Dndice%20del%20curso%206
customColor #10b981
customTextColor #ecfdf5
```