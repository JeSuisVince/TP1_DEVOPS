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
docker pull tomcat
cp  Dockerfil tomcat
