## Ejercicio 5

`HEALTHCHECK`: Permite establecer un comando establecido por el usuario que verifica si el proceso de un contenedor está corriendo correctamente. Por ejemplo, si el proceso queda en un bucle infinito por algún motivo, con este comando Docker agregará al status un indicador que el contenedor no se encuentra "saludable".

HEALTHCHECK recibe como argumentos cada cuánto se corre el check, la cantidad y tiempo de reintentos ante un error, tiempo de inicio y comando que se correrá para hacer el check.

Este check es información que Docker conoce pero no hace nada si detecta que un contenedor no se encuentra saludable. Esta información puede ser usada por orquestadores.

`ONBUILD`: La instrucción que recibe se correrá cuando la imagen se use como base para la construcción de otra imagen. Estas instrucciones se ejecutarán inmediatamente luego de la instrucción FROM de la construcción de la imagen "hija". Por ejemplo, se puede usar para estandarizar el uso de una imagen, estableciendo dónde se debe copiar el código.

`VOLUME`: Recibe uno o varios directorios del lado del contenedor, los cuales montará como volúmenes de Docker. En este caso, la información que se copie a estos directorios persistirá incluso si el contenedor muere y podrá trasladarse.
