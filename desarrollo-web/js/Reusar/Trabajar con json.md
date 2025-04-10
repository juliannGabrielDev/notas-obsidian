JSON (JavaScript Object Notation) es un formato de archivo estándar que se utiliza para representar datos estructurados. Es muy común en el desarrollo web para transmitir datos entre un servidor y una aplicación web.

**1. Leer datos de un archivo JSON:**

Para leer datos de un archivo JSON en JavaScript, puedes usar el método `fetch()` para obtener el archivo y luego el método `json()` para analizar el contenido como JSON.

```
fetch('data.json') // Reemplaza 'data.json' con la ruta de tu archivo
  .then(response => response.json())
  .then(data => {
    // Aquí puedes trabajar con los datos del archivo JSON
    console.log(data);
  })
  .catch(error => {
    // Maneja cualquier error que ocurra durante la lectura del archivo
    console.error('Error al leer el archivo JSON:', error);
  });
```

**2. Analizar una cadena JSON:**

Si tienes una cadena que contiene datos en formato JSON, puedes usar el método `JSON.parse()` para convertirla en un objeto JavaScript.

```
const jsonString = '{"nombre": "Juan", "edad": 30, "ciudad": "México"}';
const objeto = JSON.parse(jsonString);

console.log(objeto.nombre); // Imprime "Juan"
console.log(objeto.edad);   // Imprime 30
console.log(objeto.ciudad); // Imprime "México"
```

**3. Convertir un objeto a una cadena JSON:**

Si tienes un objeto JavaScript y quieres convertirlo en una cadena JSON, puedes usar el método `JSON.stringify()`.

```
const objeto = {
  nombre: 'Juan',
  edad: 30,
  ciudad: 'México'
};

const jsonString = JSON.stringify(objeto);
console.log(jsonString);
// Imprime: {"nombre":"Juan","edad":30,"ciudad":"México"}
```

**Ejemplo completo:**

Supongamos que tienes un archivo JSON llamado `datos.json` con el siguiente contenido:

```
[
  { "nombre": "Juan", "edad": 30, "ciudad": "México" },
  { "nombre": "María", "edad": 25, "ciudad": "Guadalajara" },
  { "nombre": "Pedro", "edad": 40, "ciudad": "Monterrey" }
]
```

Aquí te mostramos cómo leer este archivo, analizar el JSON e imprimir los nombres de las personas:

```
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Leer datos JSON</title>
</head>
<body>
  <script>
    fetch('datos.json')
      .then(response => response.json())
      .then(data => {
        data.forEach(persona => {
          console.log(persona.nombre);
        });
      })
      .catch(error => console.error('Error:', error));
  </script>
</body>
</html>
```