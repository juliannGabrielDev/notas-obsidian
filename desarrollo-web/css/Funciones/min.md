---
tags:
  - css
  - funciones
---
La función `min()` en CSS se utiliza para tomar el valor mínimo de una lista de valores dados. Puede ser útil cuando se desea establecer un tamaño que no supere un límite específico.

**Por ejemplo**:

```css
/* .elemento { width: 50%; max-width: 300px; } */ 

.elemento { width: min(50%, 300px); }
```

En este caso, el ancho del elemento será el menor valor entre el 50% de su contenedor padre y 300 píxeles.