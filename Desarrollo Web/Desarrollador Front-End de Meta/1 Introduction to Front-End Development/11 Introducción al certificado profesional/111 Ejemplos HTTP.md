---
tags:
  - front-end
  - curso-1
  - modulo-1
---
## Métodos HTTP

Los métodos HTTP ==indican la **acción** que el cliente desea realizar sobre el recurso del servidor web==.

Los métodos más comunes son:

| Método HTTP | Descripción                                                      |
| ----------- | ---------------------------------------------------------------- |
| GET         | El cliente solicita un recurso en el servidor web.               |
| POST        | El cliente envía datos a un recurso en el servidor web.          |
| PUT         | El cliente sustituye un recurso en el servidor web.              |
| DELETE      | El cliente borra un recurso en el servidor web.                  |
| PATCH       | El cliente actualiza parcialmente un recurso en el servidor web. |

## Solicitud HTTP
### Línea de petición

Toda solicitud HTTP comienza con la línea de solicitud.

Ésta consta del método HTTP, el recurso solicitado y la versión del protocolo HTTP

`GET /home.html HTTP/1.1`

### Cabeceras de solicitud HTTP

Después de la línea de solicitud, las cabeceras HTTP van seguidas de un salto de línea.

Existen varias posibilidades a la hora de incluir una cabecera HTTP en la petición HTTP. ==Una **cabecera** es un nombre que no distingue entre mayúsculas y minúsculas, seguido de `:` y, a continuación, de un **valor**==.

Las cabeceras más comunes son:

```
Host: example.com
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.9; rv:50.0) Gecko/20100101 Firefox/50.0
Accept: */*
Accept-Language: en
Content-type: text/json
```

- La cabecera **Host** especifica el host del servidor e indica desde dónde se solicita el recurso.

- La cabecera **User-Agent** informa al servidor web de la aplicación que está realizando la solicitud. Suele incluir el sistema operativo (Windows, Mac, Linux), la versión y el proveedor de la aplicación.

- La cabecera **Accept** informa al servidor web del tipo de contenido que el cliente aceptará como respuesta.

- La cabecera **Accept-Language** indica el idioma y, opcionalmente, la configuración regional que prefiere el cliente.
    
- La cabecera **Content-type** indica el tipo de contenido que se transmite en el cuerpo de la solicitud.

### Cuerpo de la solicitud HTTP

Las peticiones HTTP pueden incluir opcionalmente un cuerpo de petición. A menudo se incluye un cuerpo de petición cuando se utilizan los métodos HTTP POST y PUT para transmitir datos.

```
POST /users HTTP/1.1
Host: example.com

{
 "key1":"value1",
 "key2":"value2",
 "array1":["value3","value4"]
}
```

```
PUT /users/1 HTTP/1.1
Host: example.com
Content-type: text/json

{"key1":"value1"}
```

## Respuestas HTTP

Cuando el servidor web termine de procesar la solicitud HTTP, enviará de vuelta una respuesta HTTP.

La primera línea de la respuesta es la **línea de estado**. Esta línea muestra al cliente si la solicitud se ha realizado correctamente o si se ha producido un error.

`HTTP/1.1 200 OK`

La línea comienza con la **versión** del protocolo HTTP, seguida del **código de estado** y una **frase de razón**. La frase de razón es una representación textual del código de estado.

### Códigos de estado HTTP

El primer dígito de un código de estado HTTP indica la categoría de la respuesta: **Información**, **Correcto**, **Redirección**, **Error del cliente** o **Error del servidor**.

Los códigos de estado comunes que encontrará para cada categoría son:

_1XX Informativo_

|Código de estado|Frase Razón|Descripción|
|---|---|---|
|100|Continuar|El servidor ha recibido las cabeceras de la petición y debe continuar enviando el cuerpo de la petición.|
|101|Cambiar de protocolo|El cliente ha solicitado al servidor que cambie de protocolo y el servidor ha accedido a hacerlo.|

_2XX Exitoso_

|Código de estado|Frase Razón|Descripción|
|---|---|---|
|200|OK|Respuesta estándar devuelta por el servidor para indicar que ha procesado correctamente la solicitud.|
|201|Creado|El servidor ha procesado correctamente la solicitud y se ha creado un recurso.|
|202|Aceptada|El servidor aceptó la solicitud para su procesamiento, pero éste aún no ha finalizado.|
|204|Sin contenido|El servidor ha procesado correctamente la solicitud pero no devuelve ningún contenido.|

_3XX Redirección_

|Código de estado|Frase Razón|Descripción|
|---|---|---|
|301|Movido permanentemente|Esta solicitud y todas las solicitudes futuras deben enviarse a la ubicación devuelta.|
|302|Encontrado|Esta solicitud debe enviarse a la ubicación de retorno.|

_4XX Error de cliente_

| Código de estado | Frase Razón          | Descripción                                                                                                                                                                                                                                             |
| ---------------- | -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 400              | Solicitud incorrecta | El servidor no puede procesar la solicitud debido a un error del cliente, por ejemplo, la solicitud no es válida o los datos transmitidos son demasiado grandes.                                                                                        |
| 401              | No autorizado        | El cliente que realiza la solicitud no está autorizado y debe autenticarse.                                                                                                                                                                             |
| 403              | Prohibido            | La solicitud era válida pero el servidor se niega a procesarla. Normalmente se devuelve debido a que el cliente no tiene permisos suficientes para el sitio web, por ejemplo, solicita una acción de administrador pero el usuario no es administrador. |
| 404              | No encontrado        | El servidor no ha encontrado el recurso solicitado.                                                                                                                                                                                                     |
| 405              | Método no permitido  | El servidor web no admite el método HTTP utilizado.                                                                                                                                                                                                     |

_5XX Error del servidor_

|Código de estado|Frase Razón|Descripción|
|---|---|---|
|500|Error interno del servidor|Código de estado de error genérico que se da cuando se ha producido un error o una condición inesperada al procesar la solicitud.|
|502|Puerta de enlace incorrecta|El servidor web ha recibido una respuesta no válida del servidor de aplicaciones.|
|503|Servicio no disponible|El servidor web no puede procesar la solicitud.|
### Encabezados de respuesta HTTP

Tras la línea de estado, hay cabeceras de respuesta HTTP opcionales seguidas de un salto de línea.

De forma similar a las cabeceras de solicitud, existen muchas cabeceras HTTP posibles que pueden incluirse en la respuesta HTTP.

Las cabeceras de respuesta más comunes son:

```
Date: Fri, 11 Feb 2022 15:00:00 GMT+2
Server: Apache/2.2.14 (Linux)
Content-Length: 84
Content-Type: text/html
```

- La cabecera **Date** especifica la fecha y hora en que se generó la respuesta HTTP.

- La cabecera **Server** describe el software del servidor web utilizado para generar la respuesta.

- La cabecera **Content-Length** describe la longitud de la respuesta.

- La cabecera **Content-Type** describe el tipo de medio del recurso devuelto (por ejemplo, documento HTML, imagen, vídeo).

### Cuerpo de la respuesta HTTP

A continuación de las cabeceras de respuesta HTTP se encuentra el cuerpo de la respuesta HTTP. Este es el contenido principal de la respuesta HTTP.

Puede contener imágenes, vídeo, documentos HTML y otros tipos de medios.

```
HTTP/1.1 200 OK
Date: Fri, 11 Feb 2022 15:00:00 GMT+2
Server: Apache/2.2.14 (Linux)
Content-Length: 84
Content-Type: text/html

<html>
  <head><title>Test</title></head>
  <body>Test HTML page.</body>
</html>
```