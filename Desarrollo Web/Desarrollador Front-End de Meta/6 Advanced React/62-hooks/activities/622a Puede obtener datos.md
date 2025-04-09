---
Fecha: 2024-12-31
Categoría: Reglas de los hooks y obtención de datos con hooks
tags:
  - front-end
  - curso-6
  - actividades
---
En esta actividad práctica la obtención de algunos datos de la API del sitio web randomuser.me.

Tu tarea es completar la obtención de datos usando la función `fetch()` y manejar el objeto Promise devuelto utilizando los métodos `then()`.

```jsx
import React from "react";

function App() {
  const [user, setUser] = React.useState([]);

  const fetchData = () => {
    fetch("https://randomuser.me/api/?results=1")
      .then((response) => response.json())
      .then((data) => setUser(data));
  };

  React.useEffect(() => {
    fetchData();
  }, []);

  return Object.keys(user).length > 0 ? (
    <div style={{padding: "40px"}}>
      <h1>Customer data</h1>
      <h2>Name: {user.results[0].name.first}</h2>
      <img src={user.results[0].picture.large} alt="" />
    </div>
  ) : (
    <h1>Data pending...</h1>
  );
}

export default App;
```

```button
name Índice del Curso 6
type link
action obsidian://open?vault=markdown-notes&file=desarrollo-web%2F6%20Advanced%20React%2F%C3%8Dndice%20del%20curso%206
customColor #10b981
customTextColor #ecfdf5
```