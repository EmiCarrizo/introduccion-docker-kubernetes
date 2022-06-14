## Ejercicio 2

1. Obtener la imagen fuente: `docker pull nicopaez/pingapp:3.0.0`
2. Crear repositorio en dockerhub: https://hub.docker.com/repository/docker/emilianocarrizo/taller-introduccion-docker-ejercicio02
3. Marcar la imagen para su subida: `docker tag nicopaez/pingapp:3.0.0 emilianocarrizo/taller-introduccion-docker-ejercicio02:1.0`
4. Acceder a docker mediante CLI: `docker login -u emilianocarrizo`
5. Subir la imagen a dockerhub: `docker push emilianocarrizo/taller-introduccion-docker-ejercicio02:1.0`

Cómo correr esta imagen?

```
docker run -p 4567:4567 emilianocarrizo/taller-introduccion-docker-ejercicio02:1.0
```
