### Ejecutando un contenedor en background
```
docker run -d ubuntu
```

### Ejecutando el contenedor.
```
docker run -dit ubuntu 
```
### Mostrando los contenedores ejecutandose
```
docker ps
```
### Mostrando los contenedores desplegados
```
docker ps -a
```
### Mostrando el tamañao del contenedor
```
docker ps --size
```
### Mostrando el uso de los recursos de un contenedor
```
docker stats PID
docker stats NOMBRE_DEL_CONTENEDOR
```
### Inspeccionar un contenedor en ejecución.
```
docker inspect PID
docker inspect NOMBRE_DEL_CONTENEDOR
```
### Obtener y seguir los logs de un contenedor:
```
docker logs -f <nombre_contenedor>
```

### Iniciar o detener un contenedor existente:
```
docker start PID
docker start NOMBRE_DEL_CONTENEDOR
docker stop PID
docker stop NOMBRE_DEL_CONTENEDOR
```

### Ejecutando el contenedor en un puerto personalizado.
```
docker run -it --rm -d -p 8080:80 --name web sitioweb:1.0 
```
- -it: En forma interactiva para ver los logs.
- --rm: elimina las versiones anteriores del contenedor.
- -d: el contenedor se ejecuta en un segundo plano.
- -p: mapea el puerto externo con el puerto interno(contenedor).
- --name: nombre del contenedor nombre de la imagen:versión.

### Ingresando al contenedor.
```
docker exec -ti <container-id> bash
docker attach <container-id>
```

### Eliminando un contenedor existente:
```
docker rm PID
docker rm NOMBRE_DEL_CONTENEDOR
```
