---
tags:
  - css
  - efectos
Can I Use: https://caniuse.com/?search=animation-timeline
---
```css
.animation {
    animation: nombre-de-animation linear;
    animation-timeline: view();
    animation-range: entry 0% cover 40%;
}
```

## Animación 1

Esquina inferior izquierda a esquina superior derecha.

![Imagen de la animación 1](animacion-1.png)

```css
@keyframes animation1 {
    from {
        opacity: 0;
        clip-path: inset(100% 100% 0 0);
    }
    to {
        opacity: 1;
        clip-path: inset(0 0 0 0);
    }
}
```

---

## Animación 2

Transladar el elemento 100px a la derecha.

![Imagen de la animación 2](animacion-2.png)

```css
@keyframes animation2 {
    from {
        opacity: 0;
        transform: translateX(-100px);
    }
    to {
        opacity: 1;
        transform: translateX(0);
    }
}
```

---

## Animación 3

Escalar de 0.5 a 1.

![Imagen de la animación 3](animacion-3.png)

```css
@keyframes animation3 {
    from {
        opacity: 0;
        scale: 0.5;
    }
    to {
        opacity: 1;
        scale: 1;
    }
}
```