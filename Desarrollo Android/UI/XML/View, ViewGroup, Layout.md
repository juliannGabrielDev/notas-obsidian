---
tags:
  - ui
  - xml
---
### View

Una View se define como la UI que se utiliza para crear componentes de UI interactivos como TextView, ImageView, Label, RadioButton y así sucesivamente. Se encarga del manejo de eventos y del dibujo. Generalmente se denominan "widgets".
[[Views en Android]]

### ViewGroup

Un ViewGroup sirve como clase padre para los diseños y parámetros de diseño que contienen otras Vistas o ViewGroups y definen las propiedades del diseño. Generalmente se denominan "layouts".

## Tipos de layouts de Android

### LinearLayout

LinearLayout es una subclase de ViewGroup utilizada para renderizar los elementos View hijos uno tras otro, ya sea horizontal o verticalmente, en función de la propiedad de orientación especificada.

### ConstraintLayout

ConstraintLayout es una subclase de ViewGroup utilizada para especificar la posición de las restricciones de diseño para cada vista hija en relación con otras vistas de la pantalla.

### Frame Layout

FrameLayout es una subclase de ViewGroup utilizada para especificar la posición de los elementos View que contiene unos encima de otros para mostrar una única View dentro de FrameLayout.

### Table Layout

TableLayout es una subclase de ViewGroup utilizada para mostrar los elementos View hijos en filas y columnas.

### WebView

WebView es un navegador que se utiliza para mostrar las páginas web en el diseño de su actividad.

### RecyclerView

Puede utilizar RecyclerView con LinearLayoutManager para mostrar listas desplazables de elementos en una sola columna. También puede utilizar RecyclerView con GridLayoutManager para mostrar una lista desplazable de elementos en una vista de cuadrícula de filas y columnas.