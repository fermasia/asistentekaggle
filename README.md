# Entorno para Participar en Competencias de Kaggle
Este un ejercicio de aprendizaje en el marco del Seminario de Tópicos Avanzados de la Especialización en Ciencia de Datos cursada en el Instituto Tecnológico de Buenos Aires (ITBA) en Argentina.

Los autores de este trabajo somos:

Mel, Marcos - https://github.com/mmel

Masiá, Fernando - https://github.com/fermasia - masia.fer@gmail.com

Partimos de los recursos que están disponibles en el siguiente Repositorio: https://github.com/MuttData/bigdata-workshop-es

De alli fueron eliminados los coponentes relacionados a Airflow y Kafka ya que no fuero utilizados en este proyecto. 

Las imagenes de los contenedores de Superset y Postgres fueron modificados (para que los cambios que realizamos persistan) y pusheados a una cuenta propia de DockerHub, y el script de inicialización original control-env.sh y el docker-compose.yml ajustados para utilizar estas nuevas imágenes. 

https://hub.docker.com/repository/docker/nandomasia/superset
https://hub.docker.com/repository/docker/nandomasia/postgres

Para poder acceder directamente a Superset, se creó un usuario "Admin" con la contraseña "workshop" de modo de acceder directamente al dashboard.

## Para qué sirve?

El objetivo es crear un template de Notebook de Jupyter que sirva para participar en competencias de Kaggle, que automatice parcialmente los pasos necesarios para descargar datasets, ajustar un modelo con diferentes algoritmos y parámetros, trackear estos experimentos con ayuda de MLOps, hacer submits de predicciones a Kaggle, recuperar los resultados del leaderboard y parsearlos a un Dataframe de Pandas, insertar tanto las corridas trackeadas en MLOps como los resultados obtenidos del Leaderboard de Kaggle en una base de datos Postgres, y finalmente construir un Dashboard en Superset para consultar los resultados.

## Cómo utilizar el entorno

Una vez clonado el repositorio correr el script control-env.sh con el parámetro "start".

Esto va a disponibilizar en la dirección "localhost" una homepage con los links al servidor de Jupyter Notebooks (corriendo con 2 workers de Spark) y a una insancia de Apache Superset donde estarán disponibles los Dashboards.
