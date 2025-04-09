---
tags:
  - js
  - flujo-control
---
Es algo similar a las sentencias `if…else` anidadas, pero en lugar de evaluar diferentes expresiones, `switch` evalúa una expresión condicional y luego intenta hacer coincidir su valor con uno de los casos dados. Esta es la sintaxis de la sentencia `switch`:

```js
switch (expression) {
    case first_match:
        code
        break;
    case second_match:
        code
        break;
    default:  
        code
}
```

- Además, un caso especial llamado `default` puede estar presente (por convención se coloca al final de la declaración `switch`; sin embargo, no es obligatorio).
- La evaluación en sí se realiza con un operador de comparación estricto (` === `). Por lo tanto, no solo debe coincidir el valor, sino también el tipo de valor del caso y la expresión.