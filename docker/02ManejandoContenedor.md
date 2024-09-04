### Ejecutando un contenedor en background
```
docker run -d ubuntu
```

### Ingresando al contenedor.
```
docker exec -ti <container-id> bash
docker attach <container-id>
```

### Ejecutando el contenedor.
```
docker run -dit ubuntu 
```

### Ejecutando el contenedor en un puerto personalizado.
```
docker run -it --rm -d -p 8080:80 --name web sitioweb 
```
- -it: En forma interactiva para ver los logs

- --rm: elimina las versiones anteriores del contenedor

- -d: el contenedor se ejecuta en un segundo plano

- -p: mapea el puerto del contenedor con el puerto de la aplicación para exponerla

- --name: nombre del contenedor

- Nombre de la imagen
