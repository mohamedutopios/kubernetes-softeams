## Voici une introduction à la gestion des `Dockerfile`  :

### Dockerfile
Un `Dockerfile` est un script de commandes que Docker exécute pour construire automatiquement des images. Voici les commandes les plus courantes dans un `Dockerfile` :

1. **FROM** : Définit l'image de base pour la construction de l'image.
   ```Dockerfile
   FROM ubuntu:18.04
   ```

2. **RUN** : Exécute des commandes dans le conteneur.
   ```Dockerfile
   RUN apt-get update && apt-get install -y nginx
   ```

3. **CMD** : Définit la commande par défaut à exécuter lors du démarrage du conteneur.
   ```Dockerfile
   CMD ["nginx", "-g", "daemon off;"]
   ```

4. **EXPOSE** : Informe Docker que le conteneur écoute sur les ports spécifiés.
   ```Dockerfile
   EXPOSE 80
   ```

5. **ENV** : Définit des variables d'environnement.
   ```Dockerfile
   ENV MY_VAR=my_value
   ```

6. **COPY** : Copie des fichiers et des dossiers du système de fichiers local vers l'image.
   ```Dockerfile
   COPY . /app
   ```

7. **ADD** : Copie des fichiers locaux ou télécharge des fichiers distants dans l'image.
   ```Dockerfile
   ADD https://example.com/big.tar.xz /usr/src/things/
   ```

8. **WORKDIR** : Définit le répertoire de travail pour les instructions `CMD`, `RUN`, `COPY`, `ADD`, et `ENTRYPOINT`.
   ```Dockerfile
   WORKDIR /app
   ```

9. **ENTRYPOINT** : Configure un conteneur qui sera exécuté comme un exécutable.
   ```Dockerfile
   ENTRYPOINT ["nginx"]
   ```

10. **VOLUME** : Crée un point de montage pour accéder et stocker des données persistantes.
    ```Dockerfile
    VOLUME /var/lib/mysql
    ```

