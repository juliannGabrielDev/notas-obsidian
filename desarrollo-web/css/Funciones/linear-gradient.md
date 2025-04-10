# linear-gradient()

La función `linear-gradient()` en CSS se utiliza para crear un gradiente lineal, que es una transición suave entre dos o más colores a lo largo de una línea recta. Puedes especificar la dirección del gradiente (por ejemplo, hacia la derecha, hacia abajo, en diagonal, etc.) y los colores que quieres que se mezclen. Aquí tienes un ejemplo básico:

```css
background: linear-gradient(to right, red, blue);

```

En este ejemplo, el gradiente comienza con el color rojo a la izquierda y cambia gradualmente al color azul a la derecha.

La función `linear-gradient()` en CSS se utiliza para crear un gradiente lineal, que es una transición suave entre dos o más colores a lo largo de una línea recta. Puedes especificar la dirección del gradiente (por ejemplo, hacia la derecha, hacia abajo, en diagonal, etc.) y los colores que quieres que se mezclen. Aquí tienes un ejemplo básico:

```css
background: linear-gradient(to right, red, blue);
```

En este ejemplo, el gradiente comienza con el color rojo a la izquierda y cambia gradualmente al color azul a la derecha.

Puedes personalizar aún más los gradientes lineales usando varias opciones:

1. **Dirección**: Puedes especificar la dirección del gradiente usando palabras clave como `to right`, `to bottom`, `to top right`, etc., o utilizando ángulos, como `45deg`.
2. **Múltiples colores**: No estás limitado a solo dos colores; puedes incluir tantos colores como desees.

```css
background: linear-gradient(to right, red, yelloow, green, blue);
```

3. **Posiciones de los colores**: Puedes definir puntos específicos en los que los colores deben aparecer.

```css
background: linear-gradient(to right, red 20%, yellow 50%, blue 80%);
```

4. **Transparencia**: También puedes utilizar colores con transparencia mediante valores RGBA o colores hexadecimales con un valor alfa.

```css
background: linear-gradient(to right, rgba(255, 0, 0, 0.5), rgba(0, 0, 255, 0.5));
```

5. **Repetición**: Puedes crear efectos interesantes repitiendo gradientes lineales.

```css
background: repeating-linear-gradient(45deg, red, yellow 10%, green 20%);
```

Estos son solo algunos ejemplos de cómo puedes utilizar la función `linear-gradient()` para mejorar el diseño de tu sitio web con gradientes personalizados y atractivos.

## Ejemplo útil:

```css
.hero {
	background-image: linear-gradient(rgba(0, 0, 0, 0.1), rgba(0, 0, 0, 0.6)), url(img.webp);
}
```