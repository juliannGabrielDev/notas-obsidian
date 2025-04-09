---
tags:
  - css
  - tips-and-tricks
---
## margin-inline, margin-block

```css
div {
margin-inline: auto;
margin-block: auto;
}
```

## aspect-radio

```css
.video {
	aspect-radio: 16/9;
}
```

## accent-color

```css
:root {
	accent-color: purple;
}
```

## text-underline-offset

```css
a:not([class]) {
	text-underline-offset: 0.25em;
}
```

## width: fit-content

```css
.fit-content {
  width: fit-content;
}
```

## overscroll-behavior

El uso de `overscroll-behavior: contain`aislará el desplazamiento a la región contenida, lo que evitará que continúe desplazándose a la página principal una vez que se alcance el límite de desplazamiento.

```css
.sidebar, .article {
  overscroll-behavior: contain;
}
```

## text-wrap

Tiene dos valores que resuelven el problema de composición tipográfica de líneas desequilibradas. Esto incluye la prevención de "huérfanos", que describe una palabra solitaria que se encuentra sola en la última línea de texto.

El primer valor disponible es `balance`, cuyo objetivo es equilibrar el número de caracteres por línea de texto.

Existe una limitación de seis líneas de texto ajustado, por lo que la técnica se utiliza mejor en titulares u otros pasajes de texto más breves.

```css
:is(h1, h2, h3, h4, .text-balance) {
  text-wrap: balance;
}
```

El otro valor de las `pretty`palabras huérfanas se refiere específicamente a la prevención de palabras huérfanas y se puede aplicar de manera más amplia. El algoritmo subyacente `pretty`evaluará las últimas cuatro líneas de un bloque de texto para realizar los ajustes necesarios para garantizar que la última línea tenga dos o más palabras.

```css
p {
  text-wrap: pretty;
}
```

## scrollbar-gutter

En CSS, la propiedad scrollbar-gutter se usa para controlar el espacio que ocupa la barra de desplazamiento cuando está presente, evitando cambios en el diseño al aparecer o desaparecer la barra.

```css
.contenedor {
  overflow: auto;
  scrollbar-gutter: stable;
}
```

## scrollbar-color, scrollbar-width

```css
body {
	scrollbar-color: red blue;
	scrollbar-width: auto; /*none, thin*/
}
```

## white-space

```css
span {
	white-space: nowrap;
}
```