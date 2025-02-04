### Docker Image
Les commandes d'image Docker sont utilisées pour gérer les images Docker, qui sont les bases de tous les conteneurs Docker.

1. **Lister les images** :
   ```bash
   docker image ls
   ```
   - Affiche toutes les images Docker disponibles sur votre machine.

2. **Construire une image à partir d'un Dockerfile** :
   ```bash
   docker build [options] PATH
   ```
   - Construit une image Docker à partir d'un Dockerfile. Le `PATH` spécifie l'emplacement du Dockerfile.

3. **Tirer une image depuis un registre** :
   ```bash
   docker pull IMAGE
   ```
   - Télécharge une image depuis un registre Docker comme Docker Hub.

4. **Pousser une image vers un registre** :
   ```bash
   docker push IMAGE
   ```
   - Envoie une image locale vers un registre Docker.

5. **Inspecter une image** :
   ```bash
   docker image inspect IMAGE
   ```
   - Donne des informations détaillées sur une image spécifique.

6. **Supprimer une image** :
   ```bash
   docker image rm IMAGE
   ```
   - Supprime une ou plusieurs images.

7. **Charger une image à partir d'un tarball** :
   ```bash
   docker load -i TAR_PATH
   ```
   - Charge une image à partir d'un fichier tar.

8. **Sauvegarder une image dans un tarball** :
   ```bash
   docker save -o TAR_PATH IMAGE
   ```
   - Sauvegarde une image existante dans un fichier tar.