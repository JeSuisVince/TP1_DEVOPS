# TP1_DEVOPS
tp1

Question 3

- docker pull httpd
- docker images
- mkdir docker tp 
- nano docker tp/html/index.html
'Hello world'
- docker volume create Docker_tp1
- docker run -d -v Docker_tp1:/LOCAL_PATH httpd
- docker rm Docker_tp1 (--force)
- cp Docker_tp1 httpd

Question 4 
- nano Dockerfile
''
FROM node:18-alpine
WORKDIR /app
COPY .  .
RUN npm install
CMD ["node", "src/index.js"]
EXPOSE 3000
''
- docker pull tomcat
- cp  Dockerfile tomcat
- dans les deux cas, ils sont composés de 14 couches distinctes avec Dockfil Il est facile de vérifier que la construction des images est maintenant beaucoup plus rapide et qu’elle réutilise les images déjà mises en cache.
Avec DockerFile nous pouvons build plusieurs images cest beaucoup plus "organisationnel"


Question 5 
- docker pull mysql
- docker pull phpmyadmin
- docker volume create Docker_exo1
- docker volume create Docker_exo2
- docker run -d -v Docker_exo1:/LOCAL_PATH mysql phpmyadmin
- docker run -d -v --link Docker_exo1:/LOCAL_PATH phpadmin myadmin 

Question 6 
- docker rm Docker_exo1 (--force)
- docker rm Docker_exo2 (--force)
- docker run est entièrement basé sur la ligne de commande, tandis que docker-compose lit les données de configuration à partir d'un fichier YAML.
- docker compose stop
- docker-compose up
