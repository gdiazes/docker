### Construyendo Dockerfile
Crear la carpeta html
```
mkdir html
cd html
touch index.html
echo "Hello Docker" > index.html
```
Crear el archivo Dockerfile
```
vi Dockerfile
```
Agregar el siguiente contenido:
```
FROM nginx:latest
WORKDIR /html
COPY . /usr/share/nginx/html  
```
### Creando una imagen desde el archivo Dockerfile
docker build -t <nombre_de_imagen>:version .
```
docker build -t app01:1.0 .
docker build -t app01:2.0 .
docker build -t app01:3.0 .

```
### Buscando imagen por nombre
docker images <nombre>
```
docker images app01
```

### Buscando imagen por tag
```
docker images --filter=reference='*:1.0'
```

### Mostrando el id completo de cada imagen.
```
docker images --no-trunc
```

### Cambiando el tag de una imagen.
```
docker image tag  app01:3.0 gdiaz/app01:latest
```

### Cambiando el tag de una imagen.
docker run -p <puerto_host>:<puerto_contenedor> <nombre_imagen>
```
docker run -it --rm -d -p 8080:80 app01:3.0
```

### Eliminando una imagen
```
docker rmi app01:3.0
docker rmi -f <IID>
```
