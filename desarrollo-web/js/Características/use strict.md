---
tags:
  - js
  - variables
---
```js
height = 180;
console.log(height); /* -> 180 */
```

**Puedes ver que nos hemos olvidado de declarar la variable**. La sintaxis original de JavaScript permitía tal negligencia, y en el momento de la inicialización hizo esta declaración por nosotros. **Desafortunadamente a veces puede conducir a situaciones ambiguas y potencialmente erróneas**.

## `"use strict";`

Modifiquemos nuestro ejemplo:
```js
"use strict";
height = 180; /* -> Uncaught ReferenceError: height is not defined */ console.log(height);
```

`"use strict"`; lo usamos cuando queremos forzar al intérprete a comportarse de acuerdo con los estándares modernos de JavaScript.