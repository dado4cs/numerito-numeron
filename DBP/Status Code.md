Los códigos de salida más usuales son:
- **1xx (Information):** Resultado informativo.
- **2xx (Success):** La solicitud fue recibida y aceptada correctamente.
- **3xx (Redirection):** El cliente necesita realizar acciones adicionales para completar la solicitud. Usual en oAuth2.
- **4xx (Client error):** La solicitud tiene errores que no pueden ser procesadas por el servidor. Da un *problem detail*.
- **5xx (Server error):** El servidor falló frente a una solicitud aparentemente válida

| Código | Nombre                | Descripción                                                                                                                     |
| ------ | --------------------- | ------------------------------------------------------------------------------------------------------------------------------- |
| 100    | Continue              | Servidor recibió *headers* y el cliente debe enviar el *request body*                                                           |
| 101    | Switching Protocols   | El servidor entendió y está cambiando a un protocolo diferente                                                                  |
| 102    | Processing            | El servidor recibió la respuesta y procesó la *request*, pero aun no tiene respuesta                                            |
| 103    | Early Hints           | Usado con el enlace del header permite al navegador pre-cargar los recursos mientras el servidor prepara una respuesta completa |
| 200    | OK                    | Respuesta exitosa                                                                                                               |
| 201    | Created               | Éxito y creó un nuevo recurso (común en POST)                                                                                   |
| 202    | Accepted              | Solicitud recibida y validada pero aún no se completa.                                                                          |
| 204    | No Content            | Éxito pero no devuelve contenido (común en DELETE)                                                                              |
| 300    | Multiple choices      | El recurso solicitado tiene más de una posible representación. Requiere que el usuario o el agente de usuario seleccione uno.   |
| 301    | Moved Permanently     | El recurso fue movido a una nueva URL permanentemente                                                                           |
| 302    | Found                 | El recurso reside temporalmente en otra URL                                                                                     |
| 304    | Not Modified          | El recurso no ha sido cambiado desde la última vez (usado para caché)                                                           |
| 400    | Bad Request           | El servidor no procesa la solicitud (mala sintaxis en body)                                                                     |
| 401    | Unauthorized          | Se requiere autorización para seguir la solicitud.                                                                              |
| 402    | Payment required      | Se necesita un pago para acceder a un recurso.                                                                                  |
| 403    | Forbidden             | El cliente no tiene permisos para acceder al contenido (incluso aunque esté autenticado)                                        |
| 404    | Not Found             | El servidor no encuentra el recurso                                                                                             |
| 405    | Method Not Allowed    | El método (GET, POST, ...) no está permitido para dicho cliente.                                                                |
| 409    | Conflict              | El email ya está en uso                                                                                                         |
| 422    | Unprocessable Entity  | Dato nulo o no permitido                                                                                                        |
| 429    | Too Many Requests     | El cliente ha enviado muchas solicitudes en un periodo de tiempo establecido (Rate limiting)                                    |
| 500    | Internal Server Error | Error genérico cuando el servidor no sabe como responder.                                                                       |
| 502    | Bad Gateway           | El servidor, actuando como *proxy*, recibió una respuesta inválida del servidor *upstream*.                                     |
| 503    | Service Unavailable   | El servidor no está listo para dicha petición (mantenimiento o sobrecarga)                                                      |
| 504    | Gateway Timeout       | El servidor *proxy* no recibió una respuesta a tiempo del servidor de origen                                                    |
