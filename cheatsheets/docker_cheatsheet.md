#  Docker Cheatsheet – Commandes Essentielles

---

##  **1. Images Docker**

### Lister les images
```
docker images
```

###  Télécharger une image
```
docker pull <image>
```

###  Télécharger une image avec version
```
docker pull <image>:<version>
```
Exemple :
```
docker pull redis:6.2
```

### Supprimer une image
```
docker rmi <image>
```

---

##  **2. Conteneurs**

###  Lister les conteneurs actifs
```
docker ps
```

### Lister les conteneurs actifs + stoppés
```
docker ps -a
```

### Lancer un conteneur
```
docker run <image>
```

###  Lancer en arrière‑plan
```
docker run -d <image>
```

###  Lancer avec un nom
```
docker run --name <nom> <image>
```

###  Lancer avec redirection de port
```
docker run -p <port_local>:<port_conteneur> <image>
```
Exemple :
```
docker run -p 10000:80 nginx
```

###  Suppression automatique
```
docker run --rm <image>
```

### Exemple complet Nginx
```
docker run -d --name nginx --rm -p 8080:80 nginx
```

---

##  **3. Gestion des conteneurs**

### Arrêter un conteneur
```
docker stop <nom|id>
```

###  Redémarrer un conteneur
```
docker restart <nom|id>
```

###  Supprimer un conteneur
```
docker rm <nom|id>
```

###  Logs d'un conteneur
```
docker logs <nom|id>
```

---

## **4. Construction d'images**

###  Construire une image via Dockerfile
```
docker build -t <nom_image> .
```
Exemple :
```
docker build -t my_app .
```

###  Historique d'une image
```
docker history <image>
```

---

##  **5. Projet Node.js / Python dans Docker**

###  Installer dépendances (Python)
```
pip install -r requirements.txt
```

### Lancer une app construite
```
docker run -p 10000:8000 -d my_app
```

---

## **6. Infos Docker**

###  Version Docker
```
docker version
```

###  Infos détaillées
```
docker info
```

---

## Bonus : Commandes utiles

### Suivi ressources (CPU/RAM)
```
docker stats
```

###  Ouvrir un shell dans un conteneur
```
docker exec -it <nom|id> sh
```

###  Nettoyer Docker
```
docker system prune
```

