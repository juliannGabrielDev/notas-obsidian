---
Fecha: 2024-12-21
Categoría: Renderizado de listas en React
tags:
  - front-end
  - curso-6
  - modulo-1
---

```jsx
import { useState } from "react";
import PropTypes from 'prop-types';

const ToDo = (props) => (
  <tr>
    <td>
      <label>{props.id}</label>
    </td>
    <td>
      <input />
    </td>
    <td>
      <label>{props.createdAt}</label>
    </td>
  </tr>
);

ToDo.propTypes = {
  id: PropTypes.string.isRequired,
  createdAt: PropTypes.string.isRequired
};

function App() {
  // Array de objetos que contiene los datos de los ToDos
  const [todos, setTodos] = useState([
    {
      id: "todos1",
      createdAt: "2024-01-01",
    },
    {
      id: "todos2",
      createdAt: "2024-01-02",
    },
  ]);

  // FunciÃ³n para invertir el orden de los ToDos
  const reverseOrder = () => {
    // Para evitar mutar el estado original, se crea una copia del array y se invierte
    const reversed = [...todos].reverse();
    setTodos(reversed);
    console.log(reversed);
  };

  return (
    <>
      <button onClick={reverseOrder}>Reverse</button>
      <table>
        <tbody>
          {todos.map((todo) => (
            <ToDo key={todo.id} id={todo.id} createdAt={todo.createdAt} />
          ))}
        </tbody>
      </table>
    </>
  );
}

export default App;
```