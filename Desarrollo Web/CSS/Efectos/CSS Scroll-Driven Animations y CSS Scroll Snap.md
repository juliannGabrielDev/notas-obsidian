---
tags:
  - css
  - efectos
---
```css
html {
	scroll-snap-type: y mandatory;
	timeline-scope: --section;
}
.section {
	scroll-snap-align: start;
	scroll-snap-stop: always:
	height: 100dvh;

	&:nth-child(odd) {
		background-color: red;
	}
	.content {
		overflow: hidden;
		position: fixed;
		inset: 0;
		--contrast: 4;
		--blur: 0.5rem;
		animation: blur ease-in-out both;
		animation-timeline: --section;
	}
}
@keyframes blink {
  0%,
  100% {
    filter: blur(var(--blur)) contrast(var(--contrast));
    opacity: 0;
    visibility: hidden;
  }

  50% {
    filter: blur(0) contrast(1);
    opacity: 1;
    visibility: visible;
  }
}
@keyframes horizontal-scroll {
  0% {
    transform: translate3d(100%, 0%, 0);
  }

  50% {
    transform: none;
  }

  100% {
    transform: translate3d(-100%, 0%, 0);
  }
}
@keyframes backwards-scroll {
  0% {
    transform: translate3d(0%, -100%, 0);
  }

  50% {
    transform: none;
  }

  100% {
    transform: translate3d(0%, 100%, 0);
  }
}
@keyframes zoom-scroll {
  0% {
    filter: blur(5rem);
    transform: scale(0);
    opacity: 0;
    visibility: hidden;
  }

  50% {
    filter: blur(0);
    transform: none;
    opacity: 1;
    visibility: visible;
  }

  100% {
    filter: blur(3rem);
    transform: scale(1.5);
    opacity: 0;
    visibility: hidden;
  }
}
```

## **1.`timeline-scope`**

La propiedad `timeline-scope` en CSS es parte del módulo experimental **CSS Scroll-Driven Animations** (animaciones controladas por scroll), que permite vincular animaciones al progreso del scroll o a la visibilidad de un elemento en la ventana. 

En tu ejemplo:
```css
timeline-scope: --section;
```
Estás definiendo que el elemento actual (un contenedor) **expone** la línea de tiempo (timeline) nombrada `--section` definidas en sus elementos descendientes. Esto permite que otras animaciones o elementos **fuera del contenedor** puedan acceder a esas timelines.

### **¿Para qué sirve?**

- **Propósito:** Permite que un contenedor "exponga" timelines definidas en sus elementos hijos o descendientes, para que puedan ser utilizadas por animaciones en otros lugares del documento.
- **Funcionamiento:** Las timelines se definen generalmente con propiedades como `view-timeline-name` o `scroll-timeline-name` en elementos hijos. Con `timeline-scope`, el contenedor las hace accesibles globalmente.

### **Ejemplo práctico**

Supongamos que tienes tres elementos hijos dentro de un contenedor, cada uno con su propia timeline:
```css
/* Hijos definen sus timelines */
.child-1 {
  view-timeline-name: --section; /* Timeline basada en la visibilidad del elemento */
}
.child-2 {
  scroll-timeline-name: --main; /* Timeline basada en el scroll */
}
.child-3 {
  view-timeline-name: --site-header;
}

/* Contenedor expone las timelines */
.contenedor {
  timeline-scope: --section, --main, --site-header;
}
```

Ahora, cualquier animación fuera del contenedor puede usar estas timelines:
```css
/* Animación que usa la timeline --section */
@keyframes fade-in {
  from { opacity: 0; }
  to { opacity: 1; }
}

.elemento-externo {
  animation: fade-in linear;
  animation-timeline: --section; /* Usa la timeline expuesta por el contenedor */
}
```

---

Las propiedades `scroll-snap-align` y `scroll-snap-stop` son parte del módulo **CSS Scroll Snap**, que permite controlar el desplazamiento (scroll) en contenedores para que se "ajuste" o "encaje" en puntos específicos. Aquí te explico qué hace cada una:

---

## **2. `scroll-snap-align: start;`**

- **Función:** Define **dónde se alineará el elemento hijo** dentro del contenedor cuando se realice el scroll.
- **Valores posibles:**
  - `start`: El elemento se alineará al **inicio** del contenedor (por ejemplo, la parte superior en scroll vertical o el borde izquierdo en scroll horizontal).
  - `end`: Alineación al **final** del contenedor.
  - `center`: Alineación al centro.
  - `none` (por defecto): No aplica alineación.

- **Ejemplo:**
  Si tienes un carrusel horizontal y aplicas `scroll-snap-align: start;` a los elementos hijos, cada elemento se alineará al borde izquierdo del contenedor al hacer scroll.

---

## **3. `scroll-snap-stop: always;`**

- **Función:** Controla si el scroll **debe detenerse obligatoriamente en un punto de ajuste** (snap point), incluso si el usuario hace scroll rápidamente.
- **Valores posibles:**
  - `always`: Obliga al scroll a detenerse en **todos los puntos de ajuste** que encuentre durante el desplazamiento.
  - `normal` (por defecto): Permite que el scroll pase por alto puntos de ajuste si el desplazamiento es rápido.

- **Ejemplo:**
  Si tienes una galería de imágenes donde cada imagen es un snap point, `scroll-snap-stop: always;` garantiza que el usuario no se salte ninguna imagen, incluso si desliza rápidamente.