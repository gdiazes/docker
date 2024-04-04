## Construir la imagen.
```
docker build -t <tag> .
```
## Ejemplo:
```
docker build -t apache/gdiaz .
```
## Revisar que la imagen fue construida.
```docker images```
```
REPOSITORY     TAG       IMAGE ID       CREATED         SIZE
apache/gdiaz   latest    1df5ae9c3979   9 minutes ago   278MB
```
## Ejecutando la imagen construida.
```
docker run -dit --name <nombre-a-usar> -p 8080:80 <imagen>
```
## Ejemplo:
```
docker run -dit --name wwww -p 8080:80 apache/gdiaz
```

## Identificando el ID del contenedor.
```
docker ps
```
```
CONTAINER ID   IMAGE          COMMAND                  CREATED          STATUS          PORTS                                   NAMES
d681f6a41040   apache/gdiaz   "httpd-foreground"       9 minutes ago    Up 9 minutes    0.0.0.0:8080->80/tcp, :::8181->80/tcp   www
```
## Ingresando a la images
```
docker exec -it d681f6a41040 /bin/bash
```

## Consultando la versiòn de git instalada en el contenedor.
```
root@d681f6a41040:# git --version
git version 2.39.2
```
