---
tags:
  - css
  - responsive-design
---
Las Container Queries son una característica relativamente nueva en CSS que permite aplicar estilos a un elemento en función del tamaño de su contenedor padre, en lugar de basarse únicamente en el tamaño de la ventana del navegador como lo hacen las tradicionales Media Queries.

## ¿Cómo funcionan?

 * Definición del contenedor:
   * Se asigna un nombre al contenedor usando la propiedad `container-name`.
 * Creación de la regla `@container`:
   * Se crea una regla `@container` similar a una `@media`, pero en lugar de referirse al viewport, se refiere al contenedor nombrado.
 * Aplicación de estilos:
   * Dentro de la regla `@container`, se aplican los estilos que se activarán cuando el contenedor cumpla con las condiciones especificadas.

```css
.my-container {
  container-type: inline-size;
  container-name: my-container;
}

@container my-container (width >= 600px) {
  .my-container {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
  }
}
```