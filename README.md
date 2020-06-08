# Deploy de la pagina Cafe
De esta manera deployamos nuestra web cafe con la imagen de nuestro proyecto subido a Docker Hub. Gracias a esto logramos compartir nuestro proyecto y ademas cuidar la seguridad de la misma.

## Pasos para el build de la imagen desde nuestro proyecto original
```bash
$ docker build --tag <name>:<version> .                # docker build --tag cafe:1.0.3 .
$ docker tag <name>:<version> <repositorie:version>    # docker tag cafe:1.0.3 ruizdiazever/cafe:1.0.3
$ docker login
$ docker push <repositorie:version>                    # docker push ruizdiazever/cafe:1.0.3
```

## Deployment de nuestra web desde este folder o cualquier otro
Es necesario hacer las configuraciones en docker-compose.yml
```bash
$ docker login
$ docker-compose pull
$ docker-compose -f docker-compose.yml up -d
```