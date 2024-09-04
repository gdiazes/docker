### Creando una imagen desde el archivo Dockerfile
Crear la carpeta html
```
mkdir html
cd html
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
FROM nginx:latest:

Esta línea indica que la imagen base para el contenedor será nginx en su versión más reciente (latest). Nginx es un servidor web popular que se utiliza comúnmente para servir contenido web de manera eficiente. Al usar esta imagen, el contenedor tendrá Nginx preinstalado.
VOLUME [ "/html", "/usr/share/nginx/html" ]:

Aquí se crea un volumen. Los volúmenes en Docker permiten la persistencia de datos entre los contenedores y el sistema anfitrión. En este caso, el volumen conecta el directorio /html en el sistema anfitrión con el directorio /usr/share/nginx/html dentro del contenedor, que es el directorio predeterminado donde Nginx busca archivos estáticos para servir (como páginas HTML). Esto permite que los archivos almacenados en /html en el anfitrión se reflejen automáticamente en Nginx.
ports::

Esta sección indica que se está exponiendo un puerto en el contenedor y mapeándolo a un puerto en el sistema anfitrión. No es estrictamente parte de la sintaxis del Dockerfile, sino que se usaría en un archivo de configuración de Docker Compose o como parte del comando docker run.
- 8585:80:

Esta línea especifica el mapeo de puertos. El puerto 80 es el puerto por defecto que utiliza Nginx dentro del contenedor. El puerto 8585 es el puerto en el sistema anfitrión. Al mapearlos de esta forma, cuando accedas a http://localhost:8585 en tu navegador, estarás accediendo al servidor Nginx dentro del contenedor, que está escuchando en el puerto 80.
