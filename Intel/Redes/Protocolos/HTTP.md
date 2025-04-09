# Protocolo HTTP (Hypertext Transfer Protocol)

El Protocolo de Transferencia de Hipertexto (HTTP) es un protocolo de comunicación que permite la transferencia de información en la World Wide Web.

## Características principales

- **Cliente-Servidor:** Opera mediante un modelo donde el cliente (navegador) realiza peticiones y el servidor envía respuestas.
- **Sin estado:** Cada petición HTTP es independiente y no mantiene información de peticiones anteriores.
- **Métodos HTTP:** Utiliza diferentes métodos como GET, POST, PUT, DELETE para diferentes operaciones.

## Funcionamiento básico

1. El cliente envía una petición HTTP al servidor
2. El servidor procesa la petición
3. El servidor envía una respuesta HTTP al cliente

## Códigos de estado HTTP comunes

|**Código**|**Categoría**|**Significado**|
|---|---|---|
|1XX|Informativo|La solicitud fue recibida, proceso continúa|
|100|Informativo|Continuar|
|101|Informativo|Cambiando protocolos|
|2XX|Éxito|La solicitud fue recibida y procesada correctamente|
|200|Éxito|OK|
|201|Éxito|Creado|
|204|Éxito|Sin contenido|
|3XX|Redirección|Se requieren acciones adicionales|
|301|Redirección|Movido permanentemente|
|302|Redirección|Encontrado (redirección temporal)|
|304|Redirección|No modificado|
|4XX|Error del Cliente|Error en la solicitud del cliente|
|400|Error del Cliente|Solicitud incorrecta|
|401|Error del Cliente|No autorizado|
|403|Error del Cliente|Prohibido|
|404|Error del Cliente|No encontrado|
|5XX|Error del Servidor|Error en el servidor al procesar solicitud válida|
|500|Error del Servidor|Error interno del servidor|
|502|Error del Servidor|Puerta de enlace incorrecta|
|503|Error del Servidor|Servicio no disponible|

## Versiones principales

- HTTP/1.0 - Primera versión estandarizada
- HTTP/1.1 - Introdujo conexiones persistentes
- HTTP/2 - Mayor eficiencia y multiplexación
- HTTP/3 - Basado en QUIC para mejor rendimiento

## Seguridad

HTTPS es la versión segura de HTTP, que utiliza encriptación SSL/TLS para proteger la transferencia de datos.