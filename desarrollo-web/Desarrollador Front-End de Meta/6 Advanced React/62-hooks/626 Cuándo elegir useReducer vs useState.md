---
Fecha: 2024-12-31
Categoría: Hooks avanzados
tags:
  - front-end
  - curso-6
  - modulo-2
---
El gancho `useState` se utiliza mejor con datos menos complejos.

Aunque es posible utilizar cualquier tipo de estructura de datos cuando se trabaja con `useState`, es mejor utilizarlo con tipos de datos primitivos, como cadenas, números o booleanos.

El gancho `useReducer` se utiliza mejor con datos más complejos, en concreto, matrices u objetos.

Aunque esta regla es bastante simple, hay situaciones en las que podría estar trabajando con un objeto simple y aun así decidir utilizar el gancho useState.

Tal decisión podría derivarse del simple hecho de que trabajar con `useState` a veces puede parecer más fácil que pensar en cómo se controla el estado cuando se trabaja con `useReducer`.

Podría ayudar conceptualizar este dilema como una escala gradual, en cuyo lado izquierdo se encuentra el gancho `useState` con tipos de datos primitivos y casos de uso sencillos, como activar o desactivar una variable.

En el extremo de este espectro, está el gancho `useReducer` utilizado para controlar el estado de grandes objetos que conservan el estado.

No existe un punto claro en este espectro, en el que usted decidiría: "Si mi objeto de estado tiene tres o más propiedades, utilizaré el gancho `useReducer` ".

A veces tal afirmación puede tener sentido, y otras no.

Lo que es importante recordar es que su código debe ser sencillo de entender, de colaborar en él, de contribuir a él y de construir a partir de él.

Una característica negativa de `useState` es que a menudo se vuelve difícil de mantener a medida que el estado se vuelve más complejo.

Por otro lado, una característica negativa de `useReducer` es que requiere más trabajo de preparación para empezar. Hay más configuración implicada. Sin embargo, una vez completada esta configuración, resulta más fácil ampliar el código en función de los nuevos requisitos.

## Conclusión 
---
Ha aprendido sobre el proceso de toma de decisiones a la hora de elegir entre `useReducer` y `useState` para trabajar con diferentes tipos de datos.

```button
name Índice del Curso 6
type link
action obsidian://open?vault=markdown-notes&file=desarrollo-web%2F6%20Advanced%20React%2F%C3%8Dndice%20del%20curso%206
customColor #10b981
customTextColor #ecfdf5
```