# Web App Image


### SetUp:

To start the container:

```sh
$ docker-compose -f docker-compose.yml up --build -d

$ docker-compose -f docker-compose.yml build --progress=plain
$ docker-compose -f docker-compose.yml build --no-cache --progress=plain

$ docker-compose -f docker-compose.yml up -d
```

To go inside the container

```sh
$ docker-compose -f docker-compose.yml exec web_app_image bash
```

other commands

```sh
docker container ls -a #list all the available continers 
docker stop web_app_image #stop the web_app_image continer
docker rm web_app_image #remove the web_app_image continer


docker-compose -f docker-compose.yml up -d
docker-compose -f docker-compose.yml build --no-cache --progress=plain
```


