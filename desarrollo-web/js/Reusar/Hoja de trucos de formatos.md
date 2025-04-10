## Formato de monedas

```js
/**
 * Formatea un número como precio con dos decimales.
 *
 * @param {number} precio - El precio a formatear.
 * @param {string} [localidad] - La localidad para formatear como moneda (opcional).
 * @param {string} [moneda] - La moneda para formatear (opcional).
 * @returns {string} - El precio formateado como cadena.
 */
function formatearPrecio(precio, localidad, moneda) {
  if (localidad && moneda) {
    return new Intl.NumberFormat(localidad, {
      style: 'currency',
      currency: moneda,
    }).format(precio);
  } else {
    return precio.toFixed(2);
  }
}

// Ejemplos de uso
const precio1 = 12.345;
const precio2 = 1234.567;

console.log(formatearPrecio(precio1)); // "12.35"
console.log(formatearPrecio(precio2, 'es-MX', 'MXN')); // "$1,234.57"
console.log(formatearPrecio(precio2, 'en-US', 'USD')); // "$1,234.57"
```