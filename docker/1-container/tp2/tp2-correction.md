TP -2

docker run -it -d --name nginx-web -p 8081:80 nginx
docker ps 
http://localhost:8081/
docker exec -it 5c9 /bin/bash
curl http://localhost:8081

apt update
apt install nano
cd usr/share/nginx/html/
nano index.html => MODIFIER CONTENU
http://localhost:8081/ => VERIFIER changement ok
ctrl + d => POUR QUITTER L'EXECUTION


docker search apache
docker pull httpd
docker images
docker run -it -d --name apache-mohamed -p 8082:80 httpd
docker exec -it 5cb /bin/bash
REINSTALL nano + modif -> ls, cd htdocs, nano index.html

http://localhost:8082/ => VERIFIER changement ok