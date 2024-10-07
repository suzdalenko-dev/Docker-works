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


Como construir imagenes:
    FROM indica imagen base que se utilizara para construir la nueva imagen
    RUN ejecuta comandos en la imagen
    COPY copia archivos o directorios desde host a la imagen
    WORKDIR establece el directorio de trabajo cuando se inicie un contenedor a partir de la imagen
    CMD define el comando que se ejecutra cuando se inicie un contenedor a partir de la imagen
    ENTRYPOINT define el comando que se ejecutra cuando se incio un contenedor a partir de la imagen, pero no se puede sobreescribir

    docker build . -t mi_nginx
    docker images                                           (y tengo la imagen contruida por mi "app-ingix")
    docker run -d --name mi_nginx -p 8888:80 mi_nginx     (y funciona mi propio contenedor)

    docker build . -t mypython
    docker run -it mypython
    docker start -it mypython





https://youtu.be/bd8EoJbKmwQ?list=PLQhxXeq1oc2n7YnjRhq7qVMzZWtDY7Zz0