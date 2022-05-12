# workshop-excercises-docker

Comando para crear la newtork de nginx

docker network create --driver=bridge nginx

Comando para crear el contenedor de nginx

docker container run -p 80:80 --name nginx-proxy -v /var/run/docker.sock:/tmp/docker.sock:ro --net nginx -d jwilder/nginx-proxy

Ejercicio - Parte 1

Se re requiere dockerizar un nuevo microservicio hecho en NodeJS, al cual se debe poder acceder a travez del navegador mediante una url determinada, el servidor de la aplicación NodeJs esta escuchando en el puerto 3000, el codigo del microservicio lo podemos encontrar en el siguiente repositorio.

Ejercicio - Parte 2

Se requiere armar un archivo docker-compose.yml, el cual permita levantar el microservicio creado anteriormente  junto con un contenedor de base de datos. 
En este caso el motor seleccionado será MYSQL.
Requisitos fundamentales: 
  1 - Que los datos del contenedor de mysql  se persistan una vez el contenedor se baja
  2 - Que ambos contenedores puedan comunicarse entre sí.
  3 - Que la base de datos NO pueda ser accedida a travez de internet por estricta seguridad de los datos
