## Ejercicio 11

Luego de haber deployado todos los servicios, se procede a verificar que funcione correctamente.

1. Primero obtengo el ip del clúster en minikube:
```
emiliano:~/git/intro-docker-k8s/ejercicio11 (main)  minikube ip
192.168.49.2
```
2. Luego obtengo el puerto del service asignado por kubernetes:
```
emiliano:~/git/intro-docker-k8s/ejercicio11 (main)  kube get service
NAME         TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)          AGE
kubernetes   ClusterIP   10.96.0.1        <none>        443/TCP          13d
pingapp      NodePort    10.100.216.240   <none>        8080:31830/TCP   36m
```

3. Hago los requests a la ip y puerto:
```
emiliano:~/git/intro-docker-k8s/ejercicio11 (main)  curl 192.168.49.2:31830
{"version":"2.1.0","ping":"2022-07-11T03:03:21+00:00","config_location":"/mydata/config.json","secrets_location":"/mysecrets/secret.json","host":"pingapp-6fbffd5b57-zrfkw"}
```
```
emiliano:~/git/intro-docker-k8s/ejercicio11 (main)  curl 192.168.49.2:31830/config
{
  "key1": "value1"
}
```
```
emiliano:~/git/intro-docker-k8s/ejercicio11 (main)  curl 192.168.49.2:31830/secrets
{
  "mypass": "password!"
}
```
