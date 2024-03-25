# Trabajando con imagenes.
### Images namespaces.
### Root-like. 
```
ubuntu
```
### User (and organizations)
```
gdiaz/nginx
```
### Self-Hosted
```
registry.example.com:5000/my-private-image
```
### Buscando un contenedor <ubuntu>

```
docker search ubuntu
```
```
NAME                             DESCRIPTION                                     STARS     OFFICIAL   AUTOMATED
ubuntu                           Ubuntu is a Debian-based Linux operating sys…   16419     [OK]
websphere-liberty                WebSphere Liberty multi-architecture images …   297       [OK]
open-liberty                     Open Liberty multi-architecture images based…   62        [OK]
neurodebian                      NeuroDebian provides neuroscience research s…   104       [OK]
ubuntu-debootstrap               DEPRECATED; use "ubuntu" instead                52        [OK]
ubuntu-upstart                   DEPRECATED, as is Upstart (find other proces…   115       [OK]
ubuntu/nginx                     Nginx, a high-performance reverse proxy & we…   98
ubuntu/squid                     Squid is a caching proxy for the Web. Long-t…   66
ubuntu/cortex                    Cortex provides storage for Prometheus. Long…   4
ubuntu/apache2                   Apache, a secure & extensible open-source HT…   60
ubuntu/kafka                     Apache Kafka, a distributed event streaming …   35
ubuntu/mysql                     MySQL open source fast, stable, multi-thread…   53
ubuntu/bind9                     BIND 9 is a very flexible, full-featured DNS…   62
ubuntu/prometheus                Prometheus is a systems and service monitori…   51
ubuntu/zookeeper                 ZooKeeper maintains configuration informatio…   12
ubuntu/postgres                  PostgreSQL is an open source object-relation…   31
ubuntu/redis                     Redis, an open source key-value store. Long-…   19
ubuntu/grafana                   Grafana, a feature rich metrics dashboard & …   9
ubuntu/memcached                 Memcached, in-memory keyvalue store for smal…   5
ubuntu/dotnet-aspnet             Chiselled Ubuntu runtime image for ASP.NET a…   11
ubuntu/dotnet-deps               Chiselled Ubuntu for self-contained .NET & A…   11
ubuntu/prometheus-alertmanager   Alertmanager handles client alerts from Prom…   9
ubuntu/dotnet-runtime            Chiselled Ubuntu runtime image for .NET apps…   10
ubuntu/cassandra                 Cassandra, an open source NoSQL distributed …   2
ubuntu/telegraf                  Telegraf collects, processes, aggregates & w…   4

```


### Ejecutando un contenedor de forma interactiva. <ubuntu>
#### -i tells Docker to connect us to the container's stdin.
#### -t tells Docker that we want a pseudo-terminal.

```
docker run -it ubuntu
```
```
apt-get update
```
```
apt-get install figlet
```

```
figlet  TECSUP
```
```
 _____ _____ ____ ____  _   _ ____
|_   _| ____/ ___/ ___|| | | |  _ \
  | | |  _|| |   \___ \| | | | |_) |
  | | | |__| |___ ___) | |_| |  __/
  |_| |_____\____|____/ \___/|_|

```
```
exit
```
>[!IMPORTANT]
>Después de salir del contenedor, la configuración realizada se pierde.
