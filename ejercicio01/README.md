## Ejercicio 1

Cómo correr esta imagen:

1. Asegurarse que estamos en el directorio ejercicio01
2. Correr:
```
docker run -it --rm --name nginx -v $PWD/html:/usr/share/nginx/html -v $PWD/nginx.conf:/etc/nginx/nginx.conf -p 8000:80 nginx:1
```
La página se puede visualizar en http://localhost:8000
