# Ejercicio 9

1. Primero se levanta el clúster de minikube: `minikube start`
2. Para levantar el deployment: `minikube kubectl -- apply -f ejercicio09/deployment.yaml`

Para verificar su funcionamiento:
1. Obtengo la lista de pods:
```
minikube kubectl get pods
NAME                          READY   STATUS    RESTARTS   AGE
passwordapi-5f6bdccfb-7g7mb   1/1     Running   0          14s
passwordapi-5f6bdccfb-q7tjg   1/1     Running   0          14s
passwordapi-5f6bdccfb-wqd42   1/1     Running   0          14s
```
2. Elijo uno y accedo al mismo mediante el comando: `minikube kubectl -- exec -it passwordapi-5f6bdccfb-7g7mb -- bash`
3. Una vez dentro, verifico que el proceso está corriendo: 
```
root@passwordapi-5f6bdccfb-7g7mb:/usr/src/app# curl localhost:3000/password
{"password":"!210??IiCcFf"}
```
