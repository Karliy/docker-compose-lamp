## How to use(on Mac)

```bash
# clone this repository
$ git clone https://github.com/qube81/docker-compose-lamp.git
```


### use from Vagrant (with coreOS) 

```bash
$ cd docker-compose-lamp/
$ vagrant up
# open http://localhost:8888
```


### use Docker only

```bash
# install Docker
$ curl -fsSL https://get.docker.com/ | sh

# install docker-compose
$ curl -L "https://github.com/docker/compose/releases/download/1.8.1/docker-compose-$(uname -s)-$(uname -m)" > /usr/local/bin/docker-compose
$ chmod +x /usr/local/bin/docker-compose

# build
$ cd docker-compose-lamp/docker
$ docker-compose up -d --build

# open http://localhost:8888
```

synced folder is `docker/src`.

```
(mac)docker/src <-> (Vagrant/coreOS)/tmp/docker/src <-> (Docker/php:7-apache)/var/www/html
```

links

* https://hub.docker.com/_/php/
* https://hub.docker.com/_/mysql/
