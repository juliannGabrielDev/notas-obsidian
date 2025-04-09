---
tags:
  - css
  - avanzado
---
En CSS, la regla `@layer` se utiliza para definir **capas de especificidad** (layers), que permiten organizar y controlar el orden en que se aplican los estilos. Las capas se pueden usar para gestionar la prioridad de los estilos sin depender únicamente de la especificidad o el orden en el archivo CSS.

En tu ejemplo:

```css
@layer base, rhythm, layout, components, default, overwrites;
```

Estás definiendo **6 capas** en un orden específico. El orden en que se listan las capas determina su prioridad: la primera capa (`base`) tiene la menor prioridad, y la última (`overwrites`) tiene la mayor.

### ¿Cómo funciona?
1. **Prioridad de las capas:**
   - Las capas definidas más adelante en la lista tienen mayor prioridad.
   - En tu caso, `overwrites` tendrá la mayor prioridad, seguida de `default`, `components`, etc.

2. **Definición de estilos en capas:**
   Puedes asignar estilos a una capa específica usando la sintaxis `@layer nombre_capa { ... }`. Por ejemplo:

   ```css
   @layer base {
       body {
           font-family: Arial, sans-serif;
       }
   }

   @layer components {
       .button {
           background-color: blue;
       }
   }

   @layer overwrites {
       .button {
           background-color: red; /* Este estilo tendrá prioridad sobre el de `components` */
       }
   }
   ```

3. **Especificidad dentro de las capas:**
   - Dentro de una misma capa, la especificidad y el orden de los estilos siguen siendo relevantes.
   - Sin embargo, los estilos de una capa con mayor prioridad siempre anularán los de una capa con menor prioridad, independientemente de la especificidad.

