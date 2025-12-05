# Installation 
## Docker Desktop:
** Docker Engine : ** 
Plateforme de conteneurisation qui permet de créer et de gérer des conteneurs.

** Docker CLI (client) : ** 
Interface de ligne de commande pour interagir avec Docker Engine, permettant de lancer des commandes pour gérer images et conteneurs.

** Docker GUI : **
Interface graphique qui offre une vue visuelle de vos conteneurs, images, réseaux Docker, et volumes, simplifiant la gestion de Docker pour les utilisateurs préféran une interface graphique.

# Images et Conteneurs 

** Image Docker **
"les images deviennent des conteneurs quand elles sont lancées sur Docker Engine"

Contenu: 
Des dossiers et des fihciers :
        -Les fichiers de l'OS 
        -Les programmes nécessaires à l'application
        -Le code de l'application 
Environnement d'exécution:
        -Variables d'environnement
        -Commande de démarrage
Propriétés:
Peut etre partagé et distribué
Ne peut pas etre modifier une fois créee

**Les conteneurs"

Propriétés:
Isolé: s'exécute avec ses propres processus, dépendances et système de fichiers, sans interférer avec d'autres conteneurs ou l'hote.
Léger: partagent le meme noyau de système d'exploitation de l'hote.
Modifiable:son état peut etre modifié pendant son exécution.
Ephémère: peut etre arreté et supprimé, puis un nouveau conteneur peut etre crée à partir de la meme image ou d'une image mise à jour.
Interactif et dynamique: peut etre démarrés, stoppés, redémarrés,supprimés et déplacer facilement et dynamiquement.

# Registers
un register est un système de stockage et distrubition des images docker
il existe des register privé et public
** Docker Hub : **
 -Un des plus gros register Docker
 -Contient les images officielles de la plupart des services
 -Maintenu par les auteurs en collaboration avec la communauté Docker
 -Connecté à Docker CLI par défaut
** Versionner les images **
  Une image peut avoir plusieurs versions
  Les version sont appelées: tags
  Le tag latest désigne généralement la dernière version  

# Redirection de ports (Accéder à votre conteneur depuis votre réseau)

Les conteneurs Docker sont isolé de l'hote 
Par défaut les conteneurs ne sont pas accessible depuis l'exterieur
Redirection de port: : docker run -p 10000:80 nginx