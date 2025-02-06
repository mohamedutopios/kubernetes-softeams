
### **1. Gestion de Base des Pods**

| **Commande**                               | **Description**                                 |
|--------------------------------------------|-------------------------------------------------|
| `kubectl get pods`                         | Liste tous les Pods dans le namespace par défaut. |
| `kubectl get pods -n <namespace>`          | Liste les Pods dans un namespace spécifique.     |
| `kubectl describe pod <pod-name>`          | Affiche les détails complets d'un Pod.           |
| `kubectl delete pod <pod-name>`            | Supprime un Pod spécifique.                      |
| `kubectl create -f <file>.yaml`            | Crée un Pod à partir d'un fichier YAML.          |
| `kubectl apply -f <file>.yaml`             | Applique ou met à jour un Pod depuis un fichier YAML. |

---

### **2. Accéder à l'intérieur des Pods**

| **Commande**                               | **Description**                                 |
|--------------------------------------------|-------------------------------------------------|
| `kubectl exec -it <pod-name> -- /bin/bash` | Ouvre un terminal interactif dans le Pod (si Bash est disponible). |
| `kubectl exec -it <pod-name> -- /bin/sh`   | Ouvre un shell (pour les images Alpine ou légères). |
| `kubectl logs <pod-name>`                  | Affiche les logs d'un conteneur dans le Pod.     |
| `kubectl logs -f <pod-name>`               | Affiche les logs en temps réel (équivalent de `tail -f`). |
| `kubectl logs <pod-name> -c <container-name>` | Affiche les logs d'un conteneur spécifique si le Pod en contient plusieurs. |

---

### **3. Port Forwarding et Réseaux**

| **Commande**                                     | **Description**                                                    |
|--------------------------------------------------|--------------------------------------------------------------------|
| `kubectl port-forward pod/<pod-name> <local-port>:<pod-port>` | Redirige un port local vers un port dans le Pod (ex: `8080:80`).   |
| `kubectl get pod <pod-name> -o wide`             | Affiche des informations supplémentaires comme l'adresse IP du Pod. |
| `kubectl cp <pod-name>:<path-in-pod> <local-path>` | Copie un fichier depuis le Pod vers ta machine locale.            |
| `kubectl cp <local-path> <pod-name>:<path-in-pod>` | Copie un fichier depuis ta machine locale vers le Pod.             |

---

### **4. Debugging des Pods**

| **Commande**                                      | **Description**                                                     |
|---------------------------------------------------|---------------------------------------------------------------------|
| `kubectl get events`                              | Liste les événements récents pour diagnostiquer des erreurs.        |
| `kubectl describe pod <pod-name>`                 | Détails sur les états des conteneurs, événements, et erreurs.       |
| `kubectl top pod <pod-name>`                      | Affiche la consommation des ressources (CPU/Memory) si Metrics Server est installé. |
| `kubectl exec -it <pod-name> -- env`              | Liste les variables d'environnement du Pod.                         |
| `kubectl debug pod/<pod-name> --image=busybox`    | Lance une session de debug avec une image différente (nécessite Kubernetes 1.18+). |

---

### **5. Gestion des Pods avec des Labels et Sélecteurs**

| **Commande**                                               | **Description**                                                     |
|------------------------------------------------------------|---------------------------------------------------------------------|
| `kubectl get pods --show-labels`                           | Affiche les Pods avec leurs labels.                                 |
| `kubectl get pods -l app=nginx`                            | Liste les Pods avec le label `app=nginx`.                           |
| `kubectl label pod <pod-name> environment=production`      | Ajoute ou modifie un label sur un Pod.                              |
| `kubectl delete pods -l app=nginx`                         | Supprime tous les Pods ayant un label spécifique.                   |

---

### **6. Gestion des Conteneurs Multiples dans un Pod**

| **Commande**                                      | **Description**                                                     |
|---------------------------------------------------|---------------------------------------------------------------------|
| `kubectl exec -it <pod-name> -c <container-name> -- /bin/bash` | Ouvre un shell dans un conteneur spécifique d'un Pod multi-conteneurs. |
| `kubectl logs <pod-name> -c <container-name>`     | Affiche les logs d’un conteneur spécifique dans un Pod multi-conteneurs. |

---

### **7. Redémarrage et Recréation de Pods**

| **Commande**                                      | **Description**                                                     |
|---------------------------------------------------|---------------------------------------------------------------------|
| `kubectl delete pod <pod-name>`                   | Supprime un Pod pour forcer sa recréation (si géré par un Deployment). |
| `kubectl rollout restart deployment <deployment-name>` | Redémarre tous les Pods d’un Deployment.                            |
| `kubectl replace -f <file>.yaml`                  | Remplace un Pod existant avec une nouvelle configuration.           |

---

### **8. Exemples Avancés**

- **Lister les Pods avec un filtre :**
  ```bash
  kubectl get pods --field-selector=status.phase=Running
  ```

- **Lister les Pods triés par consommation CPU :**
  ```bash
  kubectl top pods --sort-by=cpu
  ```

- **Rediriger les logs dans un fichier :**
  ```bash
  kubectl logs <pod-name> > pod-logs.txt
  ```

- **Vérifier le statut des Pods dans tous les namespaces :**
  ```bash
  kubectl get pods --all-namespaces
  ```

---

### **9. Gestion des Namespaces pour les Pods**

| **Commande**                                        | **Description**                                                     |
|-----------------------------------------------------|---------------------------------------------------------------------|
| `kubectl get pods -n <namespace>`                   | Liste les Pods dans un namespace spécifique.                        |
| `kubectl delete pod <pod-name> -n <namespace>`      | Supprime un Pod dans un namespace spécifique.                       |
| `kubectl describe pod <pod-name> -n <namespace>`    | Affiche les détails d’un Pod dans un namespace donné.               |

---

