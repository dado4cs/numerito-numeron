Un *Application Programming Interface* permite una comunicación segura y controlada entre el cliente y el servidor.

## Tipos de API
### [[Principios REST|API REST]]
API que cumple principios que permiten sus escabilidad
### SOAP API
Usa XML para intercambiar información. Es rígido pero bueno para operaciones complejas.

Las APIs más modernas usan REST porque es simple, flexible y trabaja con web tech.
## Request
Para [[Enlaces API|conectarse a un API]] se usan identificadores, siendo el más importante el **[[Enlaces API|endpoint]]**.
En el endpoint se define el método HTTP, que puede ser:
- GET: Conseguir información
- POST: Subir nueva información
- PUT : Actualizar información
- DELETE: Eliminar información
- PATCH: Actualizacion parcial (solo una parte) de información
- HEAD: Igual a un GET, pero sin el *response body*, solo recibe los *HTTP headers*
- OPTIONS: Permite conocer los clientes saber que métodos HTTP tiene permitido

Adicionalmente, dependiendo del método y API, una request puede incluir:
- **Parámetro:** Va luego de usar `?` , y separando los parámetros por `&`.
```http
{{baseurl}}/test/task?param1=10&status=available
```
- **Cuerpo:** Suele ir un código en JSON, donde se indica que se agrega en caso de POST, o que se actualiza en caso de UPDATE.
```JSON
{
	"name":"testName",
	"id":52,
	"parangaricutirimicuaro":"parangaricutirimicuaro"
}
```

## API Response
Luego de una request, la API suele enviar una respuesta, que suele ser un [[Status Code]], Response Body (en formato JSON o XML) y headers.