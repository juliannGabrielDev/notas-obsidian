## Tarea
---
Has aprendido a crear componentes y formularios controlados en React.
Ahora es el momento de poner ese conocimiento en uso y crear un formulario de registro para el restaurante Little Lemon, donde los usuarios pueden inscribirse.

El diseño y el estilo del formulario ya están predefinidos. Tienes que añadir las piezas de código que faltan para que el formulario funcione según los requisitos.
El formulario se proporciona de forma no controlada y contiene las siguientes entradas:
- Nombre
- Apellidos
- Correo electrónico
- Contraseña
- Función

```jsx
// Importa el archivo CSS para aplicar estilos
import './App.css'; 
// Importa el hook useState desde React, que permite manejar el estado del componente
import {useState} from "react"; 
// Importa la función validateEmail desde utils. Se asume que esta función valida que el email tenga el formato correcto
import {validateEmail} from "../src/utils"; 

// Componente que muestra un mensaje de error si la contraseña es muy corta
const PasswordErrorMessage = () => { 
  return ( 
    <p className="FieldError">Password should have at least 8 characters</p> 
  ); 
}; 

// Componente principal App
function App() { 
  // Estados para almacenar los valores de los campos del formulario
  const [firstName, setFirstName] = useState(""); 
  const [lastName, setLastName] = useState(""); 
  const [email, setEmail] = useState(""); 
  const [password, setPassword] = useState({ 
    value: "", // Valor de la contraseña
    isTouched: false, // Si el campo de la contraseña ha sido tocado (perdido el foco)
  }); 
  const [role, setRole] = useState("role");  // Estado para el rol, con valor inicial "role"

  // Función que verifica si el formulario es válido
  const getIsFormValid = () => { 
    return ( 
      firstName && // Verifica si hay un nombre
      validateEmail(email) && // Verifica si el email es válido
      password.value.length >= 8 && // Verifica que la contraseña tenga al menos 8 caracteres
      role !== "role" // Verifica que el rol no sea el valor por defecto
    ); 
  }; 

  // Función para limpiar todos los campos del formulario
  const clearForm = () => { 
    setFirstName(""); 
    setLastName(""); 
    setEmail(""); 
    setPassword({ 
      value: "", 
      isTouched: false, 
    }); 
    setRole("role"); 
  }; 

  // Función que maneja el envío del formulario
  const handleSubmit = (e) => { 
    e.preventDefault(); // Evita que la página se recargue
    alert("Account created!"); // Muestra una alerta de cuenta creada
    clearForm(); // Limpia el formulario
  }; 

  // Renderiza la interfaz del formulario
  return ( 
    <div className="App"> 
      <form onSubmit={handleSubmit}> 
        <fieldset> 
          <h2>Sign Up</h2> 
          {/* Campo para el primer nombre */}
          <div className="Field"> 
            <label> 
              First name <sup>*</sup> 
            </label> 
            <input 
              value={firstName} 
              onChange={(e) => { 
                setFirstName(e.target.value); // Actualiza el estado del primer nombre
              }} 
              placeholder="First name" 
            /> 
          </div> 

          {/* Campo para el apellido */}
          <div className="Field"> 
            <label>Last name</label> 
            <input 
              value={lastName} 
              onChange={(e) => { 
                setLastName(e.target.value); // Actualiza el estado del apellido
              }} 
              placeholder="Last name" 
            /> 
          </div> 

          {/* Campo para el email */}
          <div className="Field"> 
            <label> 
              Email address <sup>*</sup> 
            </label> 
            <input 
              value={email} 
              onChange={(e) => { 
                setEmail(e.target.value); // Actualiza el estado del email
              }} 
              placeholder="Email address" 
            /> 
          </div> 

          {/* Campo para la contraseña */}
          <div className="Field"> 
            <label> 
              Password <sup>*</sup> 
            </label> 
            <input 
              value={password.value} 
              type="password" 
              onChange={(e) => { 
                setPassword({ ...password, value: e.target.value }); // Mantiene isTouched y actualiza el valor
              }} 
              onBlur={() => { 
                setPassword({ ...password, isTouched: true }); // Marca isTouched en true cuando el usuario sale del campo
              }} 
              placeholder="Password" 
            /> 
            {/* Muestra el mensaje de error si el campo fue tocado y la contraseña es muy corta */}
            {password.isTouched && password.value.length < 8 ? ( 
              <PasswordErrorMessage /> 
            ) : null} 
          </div> 

          {/* Selector para el rol */}
          <div className="Field"> 
            <label> 
              Role <sup>*</sup> 
            </label> 
            <select value={role} onChange={(e) => setRole(e.target.value)}> 
              <option value="role">Role</option> 
              <option value="individual">Individual</option> 
              <option value="business">Business</option> 
            </select> 
          </div> 

          {/* Botón para enviar el formulario */}
          <button type="submit" disabled={!getIsFormValid()}> 
            Create account 
          </button> 
        </fieldset> 
      </form> 
    </div> 
  ); 
} 

// Exporta el componente App para que pueda ser utilizado en otros archivos
export default App;
```

Validación de email: 

```js
export const validateEmail = (email) => {
  return String(email)
    .toLowerCase()
    .match(
      /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
    );
};
```