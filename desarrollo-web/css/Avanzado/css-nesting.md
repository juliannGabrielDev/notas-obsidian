# CSS Nesting

El **CSS Nesting** es una característica que permite anidar selectores dentro de otros, facilitando la organización del código y reduciendo la repetición. Es similar a cómo funcionan los preprocesadores como SASS, pero ahora es parte nativa de CSS moderno (gracias al [CSS Nesting Module](https://www.w3.org/TR/css-nesting-1/)).

---

### **Sintaxis Básica**
Usa el símbolo `&` para hacer referencia al selector padre. Esto permite:

1. **Anidar elementos hijos**:
   ```css
   .card {
     color: blue;

     /* Equivale a .card .title */
     .title {
       color: red;
     }
   }
   ```

2. **Pseudo-clases y modificadores**:
   ```css
   .boton {
     background: gray;

     /* Equivale a .boton:hover */
     &:hover {
       background: darkgray;
     }

     /* Equivale a .boton.activo */
     &.activo {
       background: green;
     }
   }
   ```

3. **Pseudo-elementos**:
   ```css
   .texto::before {
     content: "★";

     /* Equivale a .texto::before:hover */
     &:hover {
       color: gold;
     }
   }
   ```

---

### **Casos de Uso Avanzados**

#### 1. **Combinar con `@media` (Responsive Design)**:
   ```css
   .contenedor {
     width: 100%;

     @media (width >= 768px) {
       width: 50%;
     }
   }
   ```

#### 2. **Anidar múltiples niveles** (¡con moderación!):
   ```css
   nav {
     ul {
       li {
         list-style: none;

         a {
           text-decoration: none;
         }
       }
     }
   }
   ```

#### 3. **Selectores compuestos**:
   ```css
   .menu {
     /* Equivale a .menu + .menu-item */
     + .menu-item {
       margin-left: 1rem;
     }
   }
   ```

---

### **Reglas Importantes**
- **El `&` es obligatorio** en pseudo-clases (`:hover`), pseudo-elementos (`::before`), o cuando se une al padre (ej: `.padre.hijo`).
- **Sin `&` al inicio**, el navegador asume que es un selector hijo/descendiente.
- **Evita anidar demasiado** (máximo 3 niveles) para no complicar la especificidad y mantenibilidad.

---

### **Ejemplo Comparativo**
#### **CSS Tradicional**:
```css
.card { color: blue; }
.card .title { color: red; }
.card:hover { background: #f0f0f0; }
```

#### **Con Nesting**:
```css
.card {
  color: blue;

  .title { color: red; }
  &:hover { background: #f0f0f0; }
}
```

---

### **Compatibilidad**
Funciona en **Chrome 112+**, **Safari 16.5+**, **Firefox 117+** y **Edge 117+**. Verifica en [Can I Use](https://caniuse.com/css-nesting).

---

### **Ventajas**
- **Código más limpio**: Agrupa estilos relacionados.
- **Menos repetición**: Evita escribir el selector padre múltiples veces.
- **Mejor mantenibilidad**: Localiza cambios fácilmente.

⚠️ **Consejo**: Úsalo con moderación para evitar selectores demasiado específicos como `.a .b .c .d { ... }`.