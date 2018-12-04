# Grupo Tesseract Boilerplate
## Laravel 5.7 + InfyOm Laravel Generator + Docker Vessel

Made with [InfyOm Laravel Generator](http://labs.infyom.com/laravelgenerator/).

## Requirements

- **Install [Docker](https://docs.docker.com/install/)**
- [Post Install Linux](https://docs.docker.com/install/linux/linux-postinstall/)
- **Install [Docker Compose](https://docs.docker.com/compose/install/)**

The Rest of the tools will run from inside the containers.

## Setup

```
# Start Vessel and prepare the environment:

cp .env.example .env
./vessel start
./vessel composer install
./vessel artisan key:generate
./vessel artisan migrate

# Prepare de Assets
./vessel yarn install
./vessel yarn run watch
```

**Access [http://localhost](http://localhost)**

### Alternative - [Laradock](https://laradock.io)

- [Laradock Setup](https://laradock.io/getting-started/#A1)

## Troubleshooting

### In case of Docker errors

```
# Stop Containers:
docker stop $(docker ps -a -q)

# Remove Containers:
docker rm $(docker ps -a -q)

# Remove Volumes:
docker volume rm $(docker volume ls -qf dangling=true)

# Remove all Images:
docker rmi $(docker images -a -q)
```

### In case you need to unistall LAMP

```
sudo apt-get remove --purge apache2 mysql-server phpmyadmin

sudo apt autoremove
```

### In case of port errors

```
# Show ports in use:
netstat -antup

# Free the ports you need, example:
sudo fuser -k local_address/protocol
sudo fuser -k 80/tcp6
```

## Useful tools and links

- [Laravel](https://laravel.com/)
- [Vessel](https://vessel.shippingdocker.com/)
- [Laravel Generator](http://labs.infyom.com/laravelgenerator/)
- [Postman](https://www.getpostman.com/)
