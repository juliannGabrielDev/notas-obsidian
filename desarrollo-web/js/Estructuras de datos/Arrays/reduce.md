Su propósito principal es **iterar sobre todos los elementos de un array y "reducirlos" a un único valor resultante**.

Piensa en él como una forma de procesar una lista para obtener un resumen o un acumulado final. Este "único valor" puede ser de cualquier tipo: un número (como una suma total), una cadena de texto, un nuevo array, un objeto, etc.

**Ejemplo**:

```js
let cart = [
	{
		name: "Product A",
		quantity: 4
	},
	{
		name: "Product B",
		quantity: 3
	},
	{
		name: "Product C",
		quantity: 2
	}
]

const totalQuantity = cart.reduce((total, item) => {
    return total + item.quantity;
}, 0);
console.log(totalQuantity);
```