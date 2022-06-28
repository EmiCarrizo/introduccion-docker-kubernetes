# Ejercicio 10

1. Se crea un nuevo bot accediendo a https://web.telegram.org/k/#@BotFather
2. Con el comando `/newbot` se crea el bot con los siguientes datos:
```
Nombre: Ejercicio10 Bot
Usuario: ejercicio10bot
Enlace: t.me/ejercicio10bot
```
3. Se prueba el token:
```
docker run --rm --name ejercicio10bot -e TELEGRAM_TOKEN="A COMPLETAR" nicopaez/telegrambot:0.0.7
```
y se envía un mensaje al bot
4. Se levanta el clúster con `minikube start`
5. Se corre el deployment: `minikube kubectl -- apply -f ejercicio10/deployment.yaml`
6. Se vuelve a hablar al bot, verificando que responde con la versión
