# clamp()

La función `clamp()` te permite establecer un tamaño de fuente mínimo, un tamaño de fuente preferido y un tamaño de fuente máximo. Esto significa que la fuente se ajustará dentro de estos límites, asegurando que siempre sea legible pero también que se adapte al espacio disponible.
Sintaxis básica:

```css
font-size: clamp(min-size, pref-size, max-size);
```

 * **min-size**: El tamaño de fuente más pequeño que deseas.
 * **pref-size**: El tamaño de fuente preferido.
 * **max-size**: El tamaño de fuente más grande que deseas.

Ejemplo:

```css
h1 {
  font-size: clamp(1rem, 3vw, 2rem);
}
```