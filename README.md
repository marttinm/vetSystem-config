# vetSystem-config

Repositorio de configuración centralizada de los microservicios de [VetSystem](https://github.com/marttinm/vetSystem-martin-marchetto).
Lo lee el `config-server` (puerto 8888) al arrancar, y cada servicio (los microservicios y el API Gateway) le pide su configuración por nombre.

| Archivo | Para quién |
| --- | --- |
| `application.yml` | Configuración compartida por todos los microservicios |
| `ms-<nombre>.yml` | Configuración propia de cada microservicio |
| `api-gateway.yml` | Puerto, rutas, CORS y Actuator del API Gateway |

Para ver la configuración que recibe un servicio: `GET http://localhost:8888/<nombre>/default`.
