# Ejercicio 8

El ejercicio consiste de dos servicios passwordapi y un balanceador, éste último escuchando en el puerto 8000

1. Para levantar la aplicación: `docker-compose.yml` en este directorio.
2. Para verificar su funcionamiento hacer `curl http://localhost:8000/health`:
```
emiliano:~/git/intro-docker-k8s (main)  curl http://localhost:8000/health
{"host":"07cd521b2c5f","loadavg":[0.09521484375,0.14111328125,0.208984375],"freemem":1535205376,"appversion":"1.0.0"}
emiliano:~/git/intro-docker-k8s (main)  curl http://localhost:8000/health
{"host":"760b9dad3540","loadavg":[0.08740234375,0.138671875,0.20751953125],"freemem":1535639552,"appversion":"1.0.0"}
```
