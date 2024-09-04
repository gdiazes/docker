### Creando una imagen desde el archivo Dockerfile
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
VOLUME [ "/html", "/usr/share/nginx/html" ]
#ports:
#  - <Host_PORT>: <Container_PORT>
ports:
  - 8585:80
```
# Dockerfile.

### FROM nginx:latest
- **Descripción:** Esta línea establece la imagen base para tu contenedor, en este caso, es la imagen oficial de **nginx**. Al utilizar `nginx:latest`, estás especificando que deseas la versión más reciente de nginx disponible en el registro de Docker Hub.
- **Importancia:** Utilizar una imagen oficial como nginx es ideal para entornos web, ya que te proporciona un servidor web listo para usar.

### VOLUME [ "/html", "/usr/share/nginx/html" ]
- **Descripción:** Esta línea crea un **volumen** en Docker que mapea el directorio local `/html` a `/usr/share/nginx/html` dentro del contenedor.
- **Importancia:** El directorio `/usr/share/nginx/html` es el directorio por defecto donde nginx sirve archivos HTML. Al mapearlo a `/html` en el host, puedes almacenar tus archivos estáticos (como HTML, CSS, imágenes, etc.) localmente y tenerlos accesibles dentro del contenedor nginx.

### ports:
#### - 8585:80
- **Descripción:** Esta línea asigna el puerto `8585` del **host** al puerto `80` del **contenedor**.
- **Importancia:** El puerto `80` es el puerto por defecto en el que nginx sirve contenido web. Al exponer el puerto `8585` en el host, puedes acceder a tu servidor nginx simplemente visitando `http://localhost:8585` en tu navegador. Esto es útil cuando deseas evitar conflictos con otros servicios que puedan estar utilizando el puerto `80` en el host.

