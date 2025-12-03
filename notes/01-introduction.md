# 1. Introduction à Docker 
## Qu'est ce que Docker?
Outil de gestion de conteneur 
Permet de créer, déployer et gérer des application dans des conteneurs
S'assurer que les applications fonctionnent de la meme manoère qlq soit l'environnement dans lequel elles sont exécutées.

## Qu'est ce qu'un conteneur ?
Un environnement permettant d'exécuter du code 
permet d'exécuter du code de manière fiale et reproductible qu'elle que soit l'infrastructure et le système d'exloitation.
similaire au concept des vm mais mlous légers et facile à demarrer car ils ne partadent le noyau et les ressources du système hote 

## Un conteneur inclut :
Le code de l'application 
Les bibliothèques et dépendances 
Configuration de l'environnement 
Binaires exécutable (python, nodes, scala ...)

## Docker et la virtualisation traditionnelle 

** VM :** Virtualisation complète de l'OS pour chaque VMs.
** Docker : ** Partage du noyau du système d'exploitation hote (plus léger, moins de ressources, plus rapide )


# 2. Dévelopement d'applications

## Les avantages de développer avec Docker

** Sans Docker **
Installation difficile des services 
Installation spécifique suivant l'OS 
Gestion des versions difficile 
Intégration de nouveaux dev difficile 

** Avec Docker **
Installet Docker 
Gestion des versions facile
Intégration de nouveaux dev facile
démarrage rapide
Plusieurs versions d'un meme service peuvent tourner en parallèle 


# 2. Dévelopement d'applications

## Les avantages de déployer avec Docker

** Sans Docker **
Gestion versions sur le serveur
Gestion de la config serveur 
Communication entre Dev et Ops 
    -Beacoup d'échanges 
    -Problèmes = échec déploiment 

** Avec Docker **
Installation de Docker sur le serveur 
Pas de configuration serveur 
Pas de versions à gérer 
Moins d'erreur de déploiment 

