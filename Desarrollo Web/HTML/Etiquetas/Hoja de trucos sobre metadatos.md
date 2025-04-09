- [[#Nombre|Nombre]]
- [[#Contenido|Contenido]]
- [[#Conjunto de caracteres|Conjunto de caracteres]]
- [[#HTTP-equiv|HTTP-equiv]]
- [[#Meta-etiquetas básicas (meta tags Para SEO)|Meta-etiquetas básicas (meta tags Para SEO)]]
- [[#etiquetas `<meta http-equiv="..."/>|etiquetas `<meta http-equiv="..."/>]]
- [[#Meta-etiquetas de diseño adaptable/móvil|Meta-etiquetas de diseño adaptable/móvil]]

La estructura de una etiqueta meta es la siguiente:

## Nombre

El nombre de la propiedad puede ser el que desee, aunque los navegadores suelen esperar un valor que entiendan y sobre el que puedan realizar una acción. Un ejemplo sería:

```html
<meta name="author" content="name"> 
```

para indicar el autor de la página. 

## Contenido

El campo de contenido especifica el valor de la propiedad. Por ejemplo, puede utilizar:

```html
<meta name="language" content="english">
```

para especificar el idioma de la página web a los motores de búsqueda. 

## Conjunto de caracteres

El charset es un campo especial que le permite especificar la codificación de caracteres utilizada en la página para que el navegador pueda mostrarla correctamente. El más utilizado es utf-8, y usted lo añadiría a su cabecera HTML de la siguiente manera: 

```html
<meta charset="UTF-8">  
```


## HTTP-equiv

Este campo significa equivalente HTTP, y se utiliza para simular cabeceras de respuesta HTTP. Es raro verlo, y se recomienda utilizar las cabeceras HTTP en lugar de las meta-etiquetas HTML http-equiv. Por ejemplo, la siguiente etiqueta indicaría al navegador que actualice la página cada 30 minutos: 

```html
<meta http-equiv="refresh" content="30">
```

## Meta-etiquetas básicas (meta tags Para SEO)

| Elemento                                                                | Descripción                                                                                                                                     |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| `<meta name="description"/>`                                            | Proporciona una breve descripción de la página web                                                                                              |
| `<meta name="title"/>`                                                  | Especifica el título de la página web                                                                                                           |
| `<meta name="author" content="name">`                                   | Especifica el autor de la página web                                                                                                            |
| `<meta name="language" content="english">`                              | Especifica el idioma de la página web                                                                                                           |
| `<meta name="robots" content="index,follow" />`                         | Indica a los motores de búsqueda cómo rastrear o indexar la página                                                                              |
| `<meta name="google"/>`                                                 | Indica a Google que no muestre el cuadro de búsqueda sitelinks al presentar los resultados de búsqueda                                          |
| `<meta name="googlebot" content="notranslate" />`                       | Indica a Google que no desea proporcionar una traducción automática si el usuario utiliza otro idioma                                           |
| `<meta name="revised" content="Sunday, July 18th, 2010, 5:15 pm" />`     | Especifica la última fecha y hora de modificación en la que se realizaron determinados cambios                                                |
| `<meta name="rating" content="safe for kids">`                          | Especifica la audiencia prevista para la página web                                                                                           |
| `<meta name="copyright" content="Copyright 2022">`                       | Especifica un aviso de copyright                                                                                                                |

---

## etiquetas `<meta http-equiv="..."/>

| Elemento                                               | Descripción                                                            |
| ------------------------------------------------------ | ---------------------------------------------------------------------- |
| `<meta http-equiv="content-type" content="text/html">` | Especifica el formato del documento devuelto por el servidor           |
| `<meta http-equiv="default-style"/>`                   | Especifica el formato del documento de estilo                          |
| `<meta http-equiv="refresh"/>`                         | Especifica la duración de la página antes de que se considere obsoleta |
| `<meta http-equiv="Content-language"/>`                | Especifica el idioma de la página                                      |
| `<meta http-equiv="Cache-Control" content="no-cache">` | Indica al navegador cómo almacenar en caché su página                  |


---

## Meta-etiquetas de diseño adaptable/móvil


```html
<meta name="format-detection" content="telephone=yes"/>
``` 

indica que los números de teléfono deben aparecer como enlaces de hipertexto en los que se puede hacer clic para realizar una llamada telefónica.


```html
<meta name="HandheldFriendly" content="true"/>
``` 

especifica que la página puede visualizarse correctamente en dispositivos móviles.


```html
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
``` 

especifica el área de la ventana en la que se puede ver el contenido de la web.