1. **Copier un fichier du système local vers un conteneur** :
   ```
   docker cp [chemin_du_fichier_local] [nom_du_conteneur]:[chemin_dans_le_conteneur]
   ```
   Exemple :
   ```
   docker cp exemple.txt monconteneur:/dossier_cible
   ```

2. **Copier un fichier d'un conteneur vers le système local** :
   ```
   docker cp [nom_du_conteneur]:[chemin_dans_le_conteneur] [chemin_du_fichier_local]
   ```
   Exemple :
   ```
   docker cp monconteneur:/fichier_source.txt /dossier_local
   ```

3. **Copier un dossier entier du système local vers un conteneur** :
   ```
   docker cp [chemin_du_dossier_local] [nom_du_conteneur]:[chemin_dans_le_conteneur]
   ```
   Exemple :
   ```
   docker cp /mon_dossier monconteneur:/dossier_cible
   ```

4. **Copier un dossier entier d'un conteneur vers le système local** :
   ```
   docker cp [nom_du_conteneur]:[chemin_dans_le_conteneur] [chemin_du_dossier_local]
   ```
   Exemple :
   ```
   docker cp monconteneur:/dossier_source /dossier_local
   ```
