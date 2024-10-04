Imagen               - es un archivo binario que contiene elementos para crear y ejecutar un Contenedor - una vez que se crea Imagen no se puede modificar ?¿
Imagen => Contenedor - es un proceso (aplicacion y sus dependencias) (instancia de una Imagen)               
Dockerfile           - es un archivo de texto con instrucciones para crear una Imagen                       


Comandos:
    docker ps
    docker ps -a
    docker run nginx            (crea un nuevo contenedor)
    docker run -d nginx         (crea un nuevo contenedor in background)
    docker attach a1fda879c215  (estar dentro del proceso del contenedor)
    docker logs a1fda879c215    (ver logs)
    docker logs a1fda879c215 -f (ver logs en vivo)

    docker run -d -p 8080:80 nginx


Como gestionar los contenedores:
    docker start c77                           (arranca contenedor previamente creado y con el puerto ya mapeado)
    docker exec c77 ls                         (interactuar con el container ya en marcha)
    docker exec c77 touch alexey.js            (interactuar con el container ya en marcha)
    docker exec -it c77 bash                   (quedarse y navegar dentro del container (abrir un terminal interactivo))

    docker run -d --name web0 -p 8000:80 nginx
    docker container prune                     (borra los contenedores parados)


Imagenes:
    docker images
    docker pull nginx                       (descargar una imagen determinada)
    docker history nginx
    docker image prune












https://youtu.be/A8oXDTDhZWU?list=PLQhxXeq1oc2n7YnjRhq7qVMzZWtDY7Zz0