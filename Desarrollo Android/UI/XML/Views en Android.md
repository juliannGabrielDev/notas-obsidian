---
tags:
  - ui
  - xml
---
## ¿Qué son las Views?

El objeto View se crea a partir de la clase View y ocupa un área rectangular de la pantalla. Es responsable del procesamiento de dibujos y eventos.

Las views es la clase base de los widgets que se utilizan para crear componentes interactivos de la interfaz de usuario, como botones o campos de texto.

## Views Android más utilizadas

Algunas de las Vistas Android más utilizadas son:

- TextView
- EditText
- Button
- ImageView
- ImageButton
- CheckBox
- RadioButton
- RecyclerView
- DatePicker and
- Spinner
## Tamaños de las views

Una view ocupa una forma rectangular, aunque el rectángulo es invisible.

`match_parent` significa que ocupará todo el espacio disponible dentro de su ViewGroup padre, mientras que `wrap_content` significa que sólo ocupará el espacio necesario para que se muestre su contenido.

## Sintaxis XML para crear una View

```xml
<ViewName
	Attribute1=Value1
	Attribute2=Value2
	Attribute3=Value3
	AttributeN=ValueN
/>
```

Tenga en cuenta que hay dos atributos que son necesarios para cada Vista. Estos son `android:layout_height` y `android:layout_width`.