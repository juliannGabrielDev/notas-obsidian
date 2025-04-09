La forma en que se envía el formulario viene determinada por dos atributos esenciales: 

### `action`

El atributo `action` especifica a qué dirección web debe enviarse el formulario. Esta dirección es la ubicación del código del lado del servidor que procesará la solicitud.

```html
<form action="/login">
</form>
```

Es importante tener en cuenta que la acción puede ser una dirección URL completa, como `https://meta.com`, una ruta absoluta, como `/login`, o una ruta relativa, como `login`. 

### `method`

El atributo method especifica qué método HTTP se utiliza para enviar el formulario; `GET` o `POST`.

El formulario utilizará por defecto el método HTTP `GET` cuando no se proporcione el atributo method. 

Como ya sabrá, cuando el formulario se envía utilizando el método HTTP `GET`, **los datos de los campos del formulario se codifican en la URL**. Y cuando el formulario se envía utilizando el método HTTP `POST`, **los datos se envían como parte del cuerpo de la petición HTTP**. Cuando el servidor web recibe la solicitud, procesa los datos y devuelve una respuesta HTTP. 
