Imagen               - es un archivo binario que contiene elementos para crear y ejecutar un Contenedor     
Imagen => Contenedor - es un proceso (aplicacion y sus dependencias) (instancia de una Imagen)               
Dockerfile           - es un archivo de texto con instrucciones para crear una Imagen                       

Comandos:
    docker images
    docker ps
    docker ps -a
    docker run nginx            (crea un nuevo contenedor)
    docker run -d nginx         (crea un nuevo contenedor in background)
    docker attach a1fda879c215  (estar dentro del proceso del contenedor)
    docker logs a1fda879c215    (ver logs)
    docker logs a1fda879c215 -f (ver logs en vivo)

    docker run -d -p 8080:80 nginx