# Dark Souls BossPedia Server

## [Link!](https://github.com/AlejandroCorrea21/dark-souls-bosspedia-server.git)

# Descripción

DarkSouls BossPedia Server se encarga de tener toda la base de datos del cliente de Dark Souls Bosspedia.

# Estructura del Proyecto

.env
.gitignore.
db.json
package-lock.json
package.json
server.js

# Server Route Planning
API base URL hhtp://localhost:5005

Method          URL                         Request Body            Description
GET             /bosses                         n/a                 Retorna array de todos los jefes
GET             /bosses:id                      n/a                 Retorna los detalles de un jefe
                                                                        en específico segun ID
GET             /comments?bossId=value          n/a                 Retorna los comentarios de un jefe
                                                                        en específico, filtrado por ID

POST            /comments                       {"id","bossId",     Crear un comentario para un jefe
                                                                            en específico.
                                                "text","author"}

PUT             /comments/:commentid            {"id","bossId",     Actualizar comentarios de UN jefe
                                                                            en específico.
                                                "text","author"}
DELETE          /comments/:commentid            n/a                 Borrar un comentario en específico
GET             /comments?bossId=value          n/a                 Pedir todos los comentarios y
                                                                    mostrar el jefe al que se hizo
                                                                            cada comentario.
GET             /comments?_expand=boss          n/a                 Hacer página donde aparezcan todos
                                                                    los comentarios, y en los comentarios a que jefe le estan
                                                                    haciendo esos comentarios.

# Extra Links

### Excalidraw
[Link](https://excalidraw.com/#json=EcEtPPmcRkfdwosh8KufH,EyWv-fYgPPF9cAPYlYk3Hg)

## Deploy
[Link](https://dark-souls-bosspedia-server.onrender.com)

