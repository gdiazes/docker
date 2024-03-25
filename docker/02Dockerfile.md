# Trabajando con imagenes.
### Dockerfile.

```
FROM nginx:latest

# Path: /usr/share/nginx/html
COPY /html /usr/share/nginx/html  

```
### Eliminado unaimagen.
```
docker rmi -f <id>
```
### Creando la imagen.
```
docker build . -t gdiaz:latest
docker images
```
### -t = tageado.

```
docker images --no-trunc
docker image tag <origen> <destino>
docker image tag web:latest gdiaz/web:latest
```
### untag - rmi(remove image - es necesario detener la imagen.)
```
docker rmi -f <id>
docker rmi gdiaz/web:latest
```
### Levantando el contenedor
```
docker run -t -i --rm  gdiaz bash
```
