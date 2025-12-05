Gestion des Images Docker
Lister les images

docker images — Affiche toutes les images disponibles localement.

Télécharger une image depuis Docker Hub

docker pull <nom_image> — Télécharge la dernière version de l'image.

docker pull redis:6.2 — Télécharge une version spécifique.

Construire une image depuis un Dockerfile

docker build -t my_app . — Construit une image nommée my_app à partir du Dockerfile dans le répertoire courant.

Gestion des Conteneurs
Lancer un conteneur

docker run -d --name nginx --rm nginx — Lance un conteneur en mode détaché, supprimé automatiquement à l'arrêt.

docker run -p 10000:80 nginx — Expose le port 80 du conteneur sur le port 10000 de l’hôte.

docker run -p 10000:8000 -d my_app — Exécute l’image personnalisée my_app.

Lister les conteneurs

docker ps — Conteneurs actifs.

docker ps -a — Conteneurs actifs + inactifs.

Logs d’un conteneur

docker logs <nom_conteneur>

Exemple : docker logs hungry_haibt

Installation des dépendances (exemple Python)

pip install -r requirements.txt

Utilisé avant la génération d’une image pour installer toutes les dépendances.

Notes Complémentaires
Recharger une image après modification

docker build --no-cache -t my_app .

Nettoyer (images / conteneurs / volumes)

docker system prune — Supprime les ressources inutilisées (!! attention).

Libérer un port déjà occupé

docker ps -a → identifier le conteneur bloquant

docker stop <id>