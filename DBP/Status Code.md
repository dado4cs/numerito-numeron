Los códigos de salida más usuales son:
- **2xx (Success):** La solicitud fue recibida y aceptada correctamente.
- **3xx (Redirection):** El cliente necesita realizar acciones adicionales para completar la solicitud.
- **4xx (Client error):** La solicitud tiene errores que no pueden ser procesadas por el servidor
- **5xx (Server error):** El servidor falló frente a una solicitud aparentemente válida

| Código | Nombre                | Descripción                                                                                  |
| ------ | --------------------- | -------------------------------------------------------------------------------------------- |
| 200    | OK                    | Respuesta exitosa                                                                            |
| 201    | Created               | Éxito y creó un nuevo recurso (común en POST)                                                |
| 204    | No Content            | Éxito pero no devuelve contenido (común en DELETE)                                           |
| 301    | Moved Permanently     | El recurso fue movido a una nueva URL permanentemente                                        |
| 302    | Found                 | El recurso reside temporalmente en otra URL                                                  |
| 304    | Not Modified          | El recurso no ha sido cambiado desde la última vez (usual en caché)                          |
| 400    | Bad Request           | El servidor no procesa la solicitud (mala sintaxis)                                          |
| 401    | Unauthorized          | Se requiere autorización para seguir la solicitud                                            |
| 403    | Forbidden             | El cliente no tiene permisos para acceder al contenido (incluso aunque esté autentitcado)    |
| 404    | Not Found             | El servidor no encuentra el recurso solicitado                                               |
| 405    | Method Not Allowed    | El método (GET, POST, ...) no está permitido para el recurso                                 |
| 429    | Too Many Requests     | El cliente ha enviado muchas solicitudes en un periodo de tiempo establecido (Rate limiting) |
| 500    | Internal Server Error | Error genérico cuando el servidor no sabe como responder                                     |
| 502    | Bad Gateway           | El servidor, actuando como *proxy*, recibió una respuesta inválida del servidor *upstream*   |
| 503    | Service Unavailable   | El servidor no está listo para dicha petición (mantenimiento o sobrecarga)                   |
| 504    | Gateway Timeout       | El servidor *proxy* no recibió una respuesta a tiempo del servidor de origen                 |
