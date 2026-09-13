# Laboratorio 02

En este laboratorio usamos Docker Compose para levantar 3 APIs y una base de datos PostgreSQL.

Las APIs creadas son:

* api1: puerto 3000
* api2: puerto 3002
* api3: puerto 3003

Cada API muestra un mensaje diferente.

En el archivo `.env` colocamos los nombres, la base de datos, el usuario y la contraseña.

También agregamos PostgreSQL en el puerto 5432.

Para guardar los datos usamos un volumen llamado `postgresData`.

Para iniciar el proyecto usamos `docker compose up -d --build`.

Para revisar los contenedores usamos `docker ps`.

Para revisar los servicios usamos `docker compose ps`.

Para ver el volumen usamos `docker volume ls`.

Cuando terminamos, usamos `docker compose down` para detener los servicios.

Al final tenemos las 3 APIs y PostgreSQL funcionando.


## README. Responder los tipos de redes y los tipos de volumen que existen en docker

## Tipos de redes

Docker tiene varias formas de conectar los contenedores

- **bridge:** Es la más usada. Conecta contenedores que están en la misma máquina
- **host:** El contenedor usa la red del equipo principal, como si fuera él
- **overlay:** Conecta contenedores que están en equipos diferentes
- **macvlan:** Le da al contenedor su propia dirección MAC. Aparece en la red como otro dispositivo más
- **none:** Deja al contenedor sin red.

## Tipos de volúmenes

Sirven para guardar la info de los contenedores

- **Volume nombrado:** Lo administra Docker. Es el mejor para cosas importantes como una base de datos
- **Bind mount:** Conecta una carpeta de tu PC con el contenedor. Se usa mucho para programar
- **tmpfs:** Guarda todo en la RAM. Cuando apagas el contenedor se borra todo.
## Capturas de prueba
![alt text](image.png)

![alt text](image-1.png)

![alt text](image-2.png)

![alt text](image-3.png)

![alt text](image-4.png)