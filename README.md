# conversao-distancia

docker push henriqueandradesilva/conversao-distancia:v2

# docker hub
docker pull henriqueandradesilva/conversao-distancia:v1
docker pull henriqueandradesilva/conversao-distancia:latest

# comandos
docker build -t conversao-distancia -f Dockerfile .
docker container run -d -p 8080:5000 conversao-distancia
docker login
docker build -t henriqueandradesilva/conversao-distancia:v1 .
docker push henriqueandradesilva/conversao-distancia:v1
docker tag henriqueandradesilva/conversao-distancia:v1 henriqueandradesilva/conversao-distancia:latest
docker image ls
docker push henriqueandradesilva/conversao-distancia:latest
docker image rm $(docker image ls -q)
docker system prune 
docker container run -d -p 8080:5000 henriqueandradesilva/conversao-distancia:v1