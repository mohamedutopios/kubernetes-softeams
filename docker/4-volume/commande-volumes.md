### Docker Volumes
Les volumes Docker sont utilisés pour persister des données générées et utilisées par les conteneurs Docker. Voici les commandes principales pour gérer les volumes Docker :

1. **Créer un volume** :
   ```bash
   docker volume create my_volume
   ```

2. **Lister les volumes** :
   ```bash
   docker volume ls
   ```

3. **Inspecter un volume** :
   ```bash
   docker volume inspect my_volume
   ```
   - Affiche des informations détaillées sur un volume spécifique.

4. **Supprimer un volume** :
   ```bash
   docker volume rm my_volume
   ```
   - Supprime un volume. Les volumes non utilisés peuvent être supprimés en toute sécurité sans affecter les données des conteneurs actifs.

5. **Nettoyer les volumes non utilisés** :
   ```bash
   docker volume prune
   ```
   - Supprime tous les volumes non utilisés pour libérer de l'espace disque.