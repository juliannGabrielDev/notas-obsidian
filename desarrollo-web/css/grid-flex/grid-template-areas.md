# grid-template-areas

La propiedad `grid-template-areas` suele colocarse dentro de la etiqueta body o de cualquier contenedor donde deba colocarse la rejilla, del mismo modo que definiría las reglas para la rejilla. La principal diferencia es que, en el caso de `grid-template-areas` los valores presentes serán los distintos nombres.

## Proceso

El proceso no es prescriptivo pero estos son los pasos en general:

- Defina la rejilla utilizando la propiedad `display`.
- Establezca la altura y la anchura de la rejilla.
- Establezca las áreas de la plantilla de cuadrícula con los identificadores de nombre apropiados.
- Añada los tamaños adecuados para las filas dentro de la cuadrícula utilizando la propiedad `grid-template-rows`.
- Añada los tamaños apropiados para las columnas dentro de la rejilla utilizando la propiedad `grid-template-columns`.

```html
<body>
	<header> Header </header>
	<nav class="nav-bar"> Navigation </nav>
	<main> Main area </main>
	<footer> Footer </footer>
</body>
```

```css
body {
	display: grid;
	height: 200px;
	grid-template-areas:"head head"
						"aside main"
						"footer footer";
	grid-template-rows: 30px 1fr 30px;
	grid-template-columns: 150px 1fr;
}

header {
	grid-area: head;
	background-color: lightsalmon;
}

aside {
	grid-area: aside;
	background-color: lightblue;
}
main {
	grid-area: main;
	background-color: lightyellow;
}

footer {
	grid-area: footer;
	background-color: firebrick;
}
```