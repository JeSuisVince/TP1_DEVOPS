# TP1_DEVOPS
tp1

question 3

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
- nano Dockerfil
''
FROM node:18-alpine
WORKDIR /app
COPY .  .
RUN npm install
CMD ["node", "src/index.js"]
EXPOSE 3000
''
- docker pull tomcat
- cp  Dockerfil tomcat
- dans les deux cas, ils sont composés de 14 couches distinctes avec Dockfil Il est facile de vérifier que la construction des images est maintenant beaucoup plus rapide et qu’elle réutilise les images déjà mises en cache.


Question 5 
- docker pull mysql
- docker pull phpmyadmin
- docker volume create Docker_exo1
- docker volume create Docker_exo2
- docker run -d -v Docker_exo1:/LOCAL_PATH mysql phpmyadmin
- docker run -d -v --link Docker_exo1:/LOCAL_PATH phpadmin myadmin 

