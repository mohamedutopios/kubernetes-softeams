
tp3

docker run -it -d --name nginx-web3 -p 8083:80 nginx
docker run -it -d --name nginx-web4 -p 8084:80 nginx
docker run -it -d --name nginx-web5 -p 8085:80 nginx


docker exec -it nginx-web3 /bin/bash
apt update
apt install wget
apt install unzip
ls
cd /usr/share/nginx/html
wget https://target-mohamed-s3.s3.eu-west-3.amazonaws.com/html5up-editorial-m2i.zip
unzip html5up-editorial-m2i.zip
cp -r html5up-editorial/* .
rm -r html5up-editorial-m2i.zip
rm -r html5up-editorial
//ctrl + d 

docker exec -it nginx-web4 /bin/bash
apt update
apt install wget
apt install unzip
ls
cd /usr/share/nginx/html
wget https://target-mohamed-s3.s3.eu-west-3.amazonaws.com/html5up-massively.zip
unzip html5up-massively.zip
y pour remplacer index.html
rm -r html5up-massively.zip
//ctrl + d 


docker exec -it nginx-web5 /bin/bash
apt update
apt install wget
apt install unzip
ls
cd /usr/share/nginx/html
wget https://target-mohamed-s3.s3.eu-west-3.amazonaws.com/html5up-paradigm-shift.zip 
unzip html5up-paradigm-shift.zip
y pour remplacer index.html
rm -r html5up-paradigm-shift.zip
//ctrl + d 

docker stop 5e8 bc0 2bc



	
