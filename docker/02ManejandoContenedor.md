### Ejecutando un contenedor en background
```
docker run -d ubuntu
```

### Ejecutando el contenedor.
```
docker run -dit ubuntu 
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

