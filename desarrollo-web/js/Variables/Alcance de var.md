---
tags:
  - js
  - variables
---
## `var`

En el caso de declaraciones de variables usando la palabra clave `var`, la situación es ligeramente diferente. La variable declarada usándola fuera de los bloques será, como en el caso de `let`, global, es decir, será visible en todas partes. Si lo declaras dentro de un bloque, entonces... bueno, normalmente volverá a ser global.

>[!WARNING]
>El problema es que `var` ==ignora los bloques de programa ordinarios y los trata como si no existieran==. Entonces, ¿en qué situación podemos declarar una variable local usando `var`? **Sólo dentro de una función**.