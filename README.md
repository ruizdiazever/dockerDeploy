# Deploy de la pagina Cafe

## Pasos para el build de la imagen desde nuestro proyecto original
```bash
$ docker build --tag <name>:<version> .                # docker build --tag cafe:1.0.1 .
$ docker tag <name>:<version> <repositorie:version>    # docker tag cafe:1.0.1 ruizdiazever/cafe:1.0.1
$ docker login
$ docker push <repositorie:version>                    # docker push ruizdiazever/cafe:1.0.1
```

## Deployment de nuestra web desde este folder
```bash
$ docker login
$ docker-compose pull
$ docker-compose -f docker-compose.yml up -d
```