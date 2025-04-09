---
tags:
  - teoria
---
## Conceptos clave del desarrollo Android

### Componente de nivel superior

La capacidad de conectarse a Internet, realizar llamadas, tomar fotografías y mucho más es posible en las aplicaciones Android con la ayuda de cuatro clases de componentes de nivel superior: ***BroadcastReceiver***, ***ContentProvider***, ***Service*** y ***Activity***. 

### Componentes de actividad

Las actividades presentan el contenido con el que los usuarios pueden interactuar en la pantalla. Son los únicos componentes que ofrecen contenido interactivo al usuario. Una Actividad representa algo que una aplicación puede hacer. Aunque una aplicación puede proporcionar más de una Actividad, muchos desarrolladores siguen un patrón de arquitectura de Actividad Única cuando crean sus aplicaciones. Esto implica que sólo se utiliza una Actividad o un número relativamente pequeño de Actividades para toda una aplicación.
[Actividades de introducción a Android](https://developer.android.com/guide/components/activities/intro-activities)

### Archivos de proyecto

- **Configuración**: definen la estructura del proyecto
- **Código**: proporcionan la lógica
- **Recursos**: proporcionan esencialmente todo lo demás.