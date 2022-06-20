## Ejercicio 7

 - ¿Cuántos contenedores se están ejecutando?

2 contenedores, `web_1` y `db_1`.

 - ¿Cuales son las imágenes en las que están basados los mencionados contenedores?

`web_1` está basado en la imagen `nicopaez/jobvacancy-ruby:1.3.0` y `db_1` en `postgres:latest`

 - ¿Puedes leer el docker-compose-jobvacancy.yml y describir lo que hace cada una de sus lineas?
   - `version: '2'`: Indica que usa la versión 2 del formato del archivo compose
   - `services`: Lista los servicios que levantarará el archivo compose actual
   - `web`: A continuación lista los atributos del servicio `web`
     - `image: nicopaez/jobvacancy-ruby:1.3.0`: 
Indica la imagen de la cual se generará el contenedor de este servicio. En este caso, `nicopaez/jobvacancy-ruby:1.3.0`
     - `links`: Lista los otros servicios a los cuales tendrá acceso el actual. También puede usarse para establecer un alias al servicio a conectar. En este caso indica que se podrá conectar al servicio `db`
     - `ports`: Indica los puertos que mapeará Docker para la conexión del huésped con el contenedor. En este caso, desde el huésped se podrá acceder a este servicio en el puerto 3000
     - `environment`: Lista variables de entorno adicionales con sus respectivos valores del servicio `web`.
     - `depends_on`: Indica los servicios que iniciará Docker Compose antes que este servicio. Esto indica que sólo levantará el servicio `ẁeb` una vez que haya iniciado correctamente el servicio `db`.
   - `db`: A continuación lista los atributos del servicio `db`
     - `image: postgres`: Indica la imagen de la cual se generará el contenedor de este servicio. En este caso, `postgres:latest`
     - `environment`: Lista variables de entorno adicionales del servicio `postgres` con sus respectivos valores.

 - Dado que cada contenedor corre en forma aislada ¿Cómo es posible que esos contenedores se vean entre sí?

Por defecto, Docker crea una red por cada configuración de compose y agrega cada contenedor a la misma. Cada servicio es alcanzable y detectable por los demás servicios.
