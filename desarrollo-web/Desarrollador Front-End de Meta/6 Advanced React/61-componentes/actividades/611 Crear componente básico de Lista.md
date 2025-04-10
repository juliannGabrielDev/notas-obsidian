---
Fecha: 2024-12-21
Categoría: Renderizado de listas en React
tags:
  - front-end
  - curso-6
---
## Tarea
---
El restaurante Little Lemon ha decidido eliminar de su menú todos los postres con muchas calorías.

En este laboratorio, vas a implementar un nuevo componente de lista, `DessertsList`, que mostrará una lista de postres con menos de 500 calorías, todos ordenados por calorías, de menor a mayor.

Los datos con los que tienes que trabajar se te han proporcionado dentro del archivo **App.js**, como un array de objetos. Cada objeto representa un postre y tiene las siguientes propiedades: `name`, `calories` y `createdAt`.

El componente `App` pasa esa información al componente `DessertsList` como una propiedad llamada `data`.

Cada elemento de la lista debe mostrar el nombre del postre y el número de calorías, ambos separados por un guión, es decir,`Chocolate Mousse - 250 cal`.

**Código de App.jsx**
```jsx
// Importa el componente DessertsList que creamos
mport DessertsList from "./DessertsList";
// Array de objetos que contiene la información de los postres
onst desserts = [
 {
   name: "Chocolate Cake",    // Nombre del postre
   calories: 400,            // Calorías
   createdAt: "2022-09-01"  // Fecha de creación
 },
 {
   name: "Ice Cream",
   calories: 200,
   createdAt: "2022-01-02",
 },
 {
   name: "Tiramisu",
   calories: 300,
   createdAt: "2021-10-03",
 },
 {
   name: "Cheesecake",
   calories: 600,
   createdAt: "2022-01-04",
 },
;
// Componente principal de la aplicación
xport default function App() {
 return (
   // div principal con una clase para estilos
   <div className="App">
     {/* Título de la lista */}
     <h2>List of low calorie desserts:</h2>
     
     {/* 
       Renderiza el componente DessertsList 
       Le pasa el array de postres como prop llamada 'data'
     */}
     <DessertsList data={desserts} />
   </div>
 );
```

**Código de DessertsList.jsx**

```jsx
// Este es un componente funcional que recibe props como parámetro
/ props.data contendrá el array de postres que viene desde App.jsx
onst DessertsList = (props) => {
   // Aquí comenzamos una cadena de métodos para procesar los datos
   const lowCaloriesDesserts = props.data
       // 1. filter() - Crea un nuevo array solo con los postres que cumplan la condición
       .filter((dessert) => {
           // Mantiene solo los postres con menos de 500 calorías
           return dessert.calories < 500;
       })
       // 2. sort() - Ordena los postres filtrados por calorías
       .sort((a, b) => { 
           // Ordena de menor a mayor calorías
           // Si el resultado es negativo, 'a' va primero
           // Si es positivo, 'b' va primero
           return a.calories - b.calories; 
       })
       // 3. map() - Transforma cada postre en un elemento <li>
       .map((dessert) => { 
           return ( 
               // Crea un elemento de lista para cada postre
               // Muestra el nombre del postre y sus calorías
               <li>
                   {dessert.name} - {dessert.calories} cal 
               </li> 
           ); 
       }); 
    // Finalmente, retorna una lista desordenada (<ul>) con todos los elementos
   return <ul>{lowCaloriesDesserts}</ul>; 

// Exporta el componente para poder importarlo en otros archivos
export default DessertsList; 
```

Conceptos clave de React que se usan aquí:

1. **Componentes:**

- App y `DessertsList` son componentes funcionales
- Cada componente retorna JSX (HTML en JavaScript)

2. **Props:**

- Es la forma de pasar datos entre componentes
- App pasa `desserts` como prop data a `DessertsList`

3. **Métodos de array:**

- `filter()`: Para filtrar elementos
- `sort()`: Para ordenar elementos
- `map()`: Para transformar elementos en JSX.