# Demonstration réseau Docker 

### Créer un réseau + y placer 2 containers + faire communiq
uer ces containers (ping) + les deconnecter du réseau + les reconnecter à un autre réseau.

- docker network create --driver <DRIVER TYPE> <NETWORK NAME>
- docker network create --driver bridge mon-bridge
- docker network ls
- docker network inspect mon-bridge
- docker run -dit --name alpine1 --network mon-bridge alpine
- docker run -dit --name alpine2 --network mon-bridge alpine
- docker network inspect mon-bridge
- docker exec alpine1 ping -c 1 172.21.0.3
- docker exec alpine2 ping -c 1 172.21.0.2
- docker network disconnect mon-bridge alpine1
- docker network disconnect mon-bridge alpine2
- docker exec alpine1 ip a
- docker network rm mon-bridge
- docker network connect bridge alpine1
- docker network connect bridge alpine2


### Demonstration avec le reseau docker host 


// On peut pas créer un reseau host : 

docker network create driver --driver host host1 => erreur

docker run -itd --name nginx1 -p 8080:80 nginx => On peut y accéder sur port 8080.

docker run -dit --name nginx1 --network host nginx => On peut y accéder sur le port 80 sans passer par un mapping de port. On peut utiliser l'adresse IP de la machine ou localhost (machine hote).


