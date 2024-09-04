# Instalación de Docker

### Actualizando la base de datos de los paquetes.
```
sudo apt update
```
- **Descripción:** Este comando actualiza la lista de paquetes disponibles y sus versiones desde los repositorios de APT. Es fundamental para asegurarse de que estás instalando las versiones más recientes y seguras de los paquetes.

### Instalando paquetes previos.
```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```
- **Descripción:** Estos paquetes son necesarios para permitir APT usar HTTPS para descargar paquetes, gestionar certificados, y trabajar con repositorios adicionales. Garantizan que el sistema pueda acceder a las fuentes seguras y gestionar el software correctamente.

### Agregar la clave GPG para el repositorio oficial de Docker.

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```
- **Descripción:** La clave GPG se usa para verificar la autenticidad de los paquetes que se descargan del repositorio de Docker. Este paso garantiza que los paquetes no han sido alterados y provienen de una fuente confiable.

### Agregar el repositorio de Docker a las fuentes de APT
```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
```
- **Descripción:** Aquí se añade el repositorio oficial de Docker a las fuentes de APT. Esto permite a tu sistema descargar e instalar Docker directamente desde sus servidores oficiales, asegurando versiones estables y actualizadas.

### Actualizando la base de datos de los paquetes.

```
sudo apt update
```
- **Descripción:** Este comando actualiza nuevamente la lista de paquetes disponibles para incluir los del repositorio de Docker añadido previamente. Es importante hacerlo después de agregar nuevas fuentes para garantizar que los paquetes se reconozcan correctamente.

### Verificar que se instalará desde el repositorio de Docker.

```
apt-cache policy docker-ce
```
- **Descripción:** Este comando muestra de dónde se descargará Docker y qué versiones están disponibles. Verifica que Docker CE (Community Edition) se obtendrá del repositorio oficial que agregaste, en lugar del repositorio predeterminado del sistema.

### Instalando Docker.

```
sudo apt install docker-ce
```
- **Descripción:** Aquí se instala Docker Community Edition. Este paquete incluye todo lo necesario para ejecutar Docker en tu sistema, permitiéndote trabajar con contenedores y gestionar tus aplicaciones de manera eficiente.

### Verificar el estado de la instalación.

```
sudo systemctl status docker
```
- **Descripción:** Este comando muestra el estado actual del servicio Docker. Si todo se ha instalado correctamente, deberías ver que el servicio Docker está activo y ejecutándose, lo que significa que ya está listo para usarse.

### Agregar el usuario actual al grupo de docker.

```
sudo groupadd docker
sudo gpasswd -a $USER docker
sudo service docker restart
exit
```
- **Descripción:** Estos comandos agregan tu usuario al grupo `docker`, permitiéndote ejecutar comandos de Docker sin necesidad de usar `sudo` constantemente. Esto mejora la experiencia de uso al reducir la necesidad de privilegios administrativos.

### Verificando la información de Docker.

```
docker info
docker version
```
- **Descripción:** Estos comandos muestran detalles sobre la instalación de Docker, como la versión instalada y las configuraciones del sistema. Te permiten confirmar que Docker está correctamente instalado y configurado para su uso.

