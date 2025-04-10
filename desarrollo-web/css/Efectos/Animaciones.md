---
tags:
  - css
  - efectos
---
```css
@keyframes animation-name {
	0%,100%{
		background-color: blue;
	}
	50% {
		background-color: green;
	}
}
```

- [[#Propiedades|Propiedades]]
	- [[#Propiedades#**1.** `animation-name`|**1.** `animation-name`]]
	- [[#Propiedades#**2.** `animation-duration`|**2.** `animation-duration`]]
	- [[#Propiedades#**3.** `animation-timing-function`|**3.** `animation-timing-function`]]
	- [[#Propiedades#**4.** `animation-delay`|**4.** `animation-delay`]]
	- [[#Propiedades#**5.** `animation-iteration-count`|**5.** `animation-iteration-count`]]
	- [[#Propiedades#**6.** `animation-direction`|**6.** `animation-direction`]]
	- [[#Propiedades#**7.** `animation-fill-mode`|**7.** `animation-fill-mode`]]
	- [[#Propiedades#**8.** `animation-play-state`|**8.** `animation-play-state`]]
	- [[#Propiedades#**9. Propiedad abreviada** `animation`|**9. Propiedad abreviada** `animation`]]
- [[#Animaciones múltiples|Animaciones múltiples]]

---

## Propiedades

### **1.** `animation-name`

Especifica el nombre de la animación que deseas aplicar a un elemento. Este nombre debe coincidir con un bloque de `@keyframes` definido previamente.

```css
@keyframes girar {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}

.elemento {
  animation-name: girar;
}
```

### **2.** `animation-duration`

Establece la duración de la animación. Puedes usar segundos (`s`) o milisegundos (`ms`).

```css
.elemento {
  animation-duration: 2s;
}
```

### **3.** `animation-timing-function`

Controla la velocidad de la animación durante su ejecución. Define cómo la animación acelera y desacelera.

- **Valores comunes**: `linear`, `ease`, `ease-in`, `ease-out`, `ease-in-out`.
- **Función personalizada**: `cubic-bezier(n,n,n,n)` para mayor control.

```css
.elemento {
  animation-timing-function: ease-in-out;
}
```

### **4.** `animation-delay`

Especifica el tiempo que debe esperar la animación antes de comenzar.

```css
.elemento {
  animation-delay: 500ms;
}
```

### **5.** `animation-iteration-count`

Define cuántas veces se reproducirá la animación.

- **Valores**: un número específico (`1`, `2`, `3`, etc.) o `infinite` para repetir indefinidamente. 

```css
.elemento {
  animation-iteration-count: infinite;
}
```

### **6.** `animation-direction`

Determina la dirección en la que se reproduce la animación.

**Valores**:
- `normal`: dirección por defecto.
- `reverse`: la animación se reproduce al revés. 
- `alternate`: alterna entre normal y reversa en cada ciclo.
- `alternate-reverse`: comienza en reversa y alterna.

```css
.elemento {
  animation-direction: alternate;
}
```

### **7.** `animation-fill-mode`

Controla cómo se aplican los estilos de la animación antes y después de su ejecución.

**Valores**:
- `none`: por defecto, los estilos no se aplican fuera de la animación.
- `forwards`: mantiene los estilos del fotograma final.
- `backwards`: aplica los estilos del primer fotograma durante el retraso (`animation-delay`).
- `both`: combina `forwards` y `backwards`.

```css
.elemento {
  animation-fill-mode: forwards;
}
```

### **8.** `animation-play-state`

Permite pausar y reanudar una animación.

**Valores**: `running` (en ejecución), `paused` (en pausa).

```css
.elemento:hover {
  animation-play-state: paused;
}
```

### **9. Propiedad abreviada** `animation`

Puedes combinar todas las propiedades anteriores en una sola línea para mayor eficiencia.

**Sintaxis**:

```
animation: name duration timing-function delay iteration-count direction fill-mode play-state;
```

---

## Animaciones múltiples

Funciona igual que la animación regular, se pueden establecer múltiples reglas.

```css
.some-class{
	animation: animation-a 2s linear infinite alternate, 
	animation-b 3s ease infinite alternate;
}
```
