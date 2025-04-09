---
tags:
  - css
  - efectos
---
## Propiedad `transform`

### Ejemplo

```css
.sample-class {
	transform: rotate(60deg);
}
```

### Transformación múltiple sobre el mismo elemento

Se pueden aplicar transformaciones para rotate(), scale() y translate() que se pueden enumerar juntas. Cada una de estas propiedades puede tener sus propios valores y las acciones darán un efecto combinado.

```css
.sample-class {
	transform: rotate(45deg) scale(1.5) translate(45px);
}
```

---

## Propiedad `transition`

La abreviatura de `transition` tiene cuatro subpropiedades siguientes, cada una de las cuales puede definirse también individualmente.

- transition-property
- transition-duration
- transition-timing-function
- transition-delay

### Sintaxis

`transition: property duration timing-function delay;`

### Ejemplo

`transition: margin-left2s ease-in-out 0.5s;`
