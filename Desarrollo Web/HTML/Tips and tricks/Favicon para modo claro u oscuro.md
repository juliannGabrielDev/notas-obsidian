```html
​<head>
	<tittle>Tu página web</tittle>
	<!-- Favicon para el modo claro -->
	​<link 
		rel="icon"
		type="image/png"
		href="favicon.png"
	>

	<!-- Favicon para el modo oscuro -->
	​<link
		rel="icon"
		type="image/png"
		href="favicon-dark.png"
		media="(prefers-color-scheme: dark)"
	>
</head>
```

Para svg:

```html
<svg 
	xmlns="http://www.w3.org/2000/svg"
	fill="currentColor"
	viewBox="0 0 128 128">
	<path d="..." />
	<style>
		svg { color: #000; }
		@media (prefers-color-scheme: dark) {
			svg { color: #fff;
		}
	</style>
</svg>
```

