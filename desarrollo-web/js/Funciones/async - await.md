**1. La palabra clave `async`**

- Se coloca antes de la declaración de una función (`async function miFuncion() { ... }` o `const miFuncion = async () => { ... }`).
- **Propósito Principal:**
    - Hace que la función **siempre devuelva una Promesa**.
        - Si la función `async` retorna un valor (ej: `return 5;`), ese valor se envuelve automáticamente en una Promesa que se resuelve con ese valor (`Promise.resolve(5)`).
        - Si la función `async` lanza un error (`throw new Error(...)`), devuelve una Promesa que es rechazada con ese error (`Promise.reject(new Error(...))`).
    - Permite usar la palabra clave `await` **dentro** de esa función. No puedes usar `await` fuera de una función `async` (excepto en el nivel superior de los módulos de JavaScript modernos).

**2. La palabra clave `await`**

- Se usa **dentro** de una función `async`, delante de una expresión que devuelve una Promesa (como una llamada a `Workspace` o a otra función `async`).
- **Propósito Principal:**
    - **Pausa la ejecución _de la función `async`_** en ese punto.
    - Espera hasta que la Promesa a la que precede se resuelva o se rechace.
    - **Si la Promesa se resuelve:** `await` devuelve el valor con el que se resolvió la Promesa. La ejecución de la función `async` continúa desde ese punto.
    - **Si la Promesa se rechaza:** `await` lanza el valor (generalmente un objeto Error) con el que se rechazó la Promesa. Este comportamiento es similar a cómo funciona `throw` en código síncrono.

```js
async function fetchProductData() {
    try {
        const response = await fetch("../data.json");
        if (!response.ok) {
            throw new Error("Network response was not ok");
        }
        const data = await response.json();
        
        console.log(data);
    } catch (error) {
        console.log(`Error loading product data: ${error}`);
    }
}
fetchProductData();
```