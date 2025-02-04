## Voici un aperçu des commandes pour `docker network` :

### Docker Network
Les commandes réseau Docker permettent de gérer les réseaux de conteneurs, ce qui est crucial pour configurer la communication entre les conteneurs.

1. **Lister tous les réseaux** :
   ```bash
   docker network ls
   ```
   - Montre tous les réseaux disponibles dans Docker.

2. **Créer un réseau** :
   ```bash
   docker network create [options] NETWORK
   ```
   - Crée un nouveau réseau. Vous pouvez spécifier le type de pilote (comme bridge, overlay, etc.) avec l'option `--driver`.

3. **Inspecter un réseau** :
   ```bash
   docker network inspect NETWORK
   ```
   - Affiche des informations détaillées sur un réseau spécifique.

4. **Connecter un conteneur à un réseau** :
   ```bash
   docker network connect [options] NETWORK CONTAINER
   ```
   - Connecte un conteneur existant à un réseau.

5. **Déconnecter un conteneur d'un réseau** :
   ```bash
   docker network disconnect [options] NETWORK CONTAINER
   ```
   - Déconnecte un conteneur d'un réseau.

6. **Supprimer un réseau** :
   ```bash
   docker network rm NETWORK
   ```
   - Supprime un réseau spécifique.



