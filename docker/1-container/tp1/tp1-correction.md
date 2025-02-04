TP -1

docker search 2048
docker pull alexwhen/docker-2048
docker images
docker run -it -d --name jeu-mohamed -p 8081:80 alexwhen/docker-2048
docker ps 
docker run -it -d --name jeu2-mohamed -p 8082:80 alexwhen/docker-2048
docker ps
http://localhost:8082/ http://localhost:8081/
docker stop 719 409
docker ps -a => Status : Exited
docker start jeu2-mohamed
docker ps
docker stop 719 
docker rm jeu2-mohamed jeu-mohamed
docker rmi alexwhen/docker-2048
docker images 
docker ps -a