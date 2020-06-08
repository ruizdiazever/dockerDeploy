# Deploy de la pagina Cafe

## Pasos para el build de la imagen  
```bash
$ docker build --tag <name>:<version>                   # cafe:1.0.0
$ docker tag <name>:<version> /<repositorie:version>    # cafe:1.0.0 /cafe:1.0.0
$ docker login
$ docker push /<repositorie:version>                    # cafe:1.0.0
```

## Deployment de nuestra web
```bash
$ docker login
$ docker-compose pull
$ docker-compose -f docker-compose.yml up -d
```