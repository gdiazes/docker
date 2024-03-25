# Instalación de Docker

### Actualizando la base de datos de los paquetes.
```
sudo apt update
```
### Instalando paquetes previos.
```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```
### Agregar la clave GPG para el respositorio oficial de Docker.
```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
### Agregar el repositorio de Docker a las fuente de APT
```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
```
### Actualizando la base de datos de los paquetess.
```
sudo apt update
```
### Verificar que se instlara desde respositorio de Docker.
```
apt-cache policy docker-ce
```
### Instalando Docker.
```
sudo apt install docker-ce
```
### Verificar el estado de la instalación.
```
sudo systemctl status docker
```
### Agregar el usuario actual al grupo de docker.
```
sudo groupadd docker
```
```
sudo gpasswd -a $USER docker
```
```
sudo service docker restart
```
```
exit
```
### Verificando la información de docker.
```
docker info
```
```
docker version
```
