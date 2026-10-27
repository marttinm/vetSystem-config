# vetSystem-config

Repositorio de configuración centralizada de los microservicios de [VetSystem](https://github.com/marttinm/vetSystem-martin-marchetto).
Lo lee el `config-server` (puerto 8888) al arrancar, y cada microservicio le pide su configuración por nombre.

| Archivo | Para quién |
| --- | --- |
| `application.yml` | Configuración compartida por todos los microservicios |
| `ms-<nombre>.yml` | Configuración propia de cada microservicio |

Para ver la configuración que recibe un servicio: `GET http://localhost:8888/<nombre>/default`.
