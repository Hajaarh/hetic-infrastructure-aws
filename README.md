# Conception et Déploiement d'une Infrastructure Cloud Sécurisée avec AWS

## Objectifs :
Ce TP a pour but de vous familiariser avec les bases de la conception d'infrastructures en utilisant des technologies de conteneurisation et de déploiement sur le cloud. Vous apprendrez à conteneuriser une application web, à la déployer sur AWS, et à mettre en place des mesures de sécurité de base, telles que la gestion des droits d'accès.


### Partie 0: Récupération du code source
- Créer un fork de ce repo: https://github.com/choucroute-volante/hetic-infra-2
- Y créer un fichier binome.md en y ajoutant les noms et prénoms de vos binômes, puis commit et push ces modifications.


### Partie 1 : Conteneurisation d'une Application Web

#### Récupération et lancement de l’app :
- Lancer l’application et vérifier son bon fonctionnement

#### Création du Dockerfile :
- Écrire un Dockerfile pour conteneuriser l'application.

#### Construction et Test de l'Image :
- Construire l'image Docker localement 
- Tester l'image en exécutant le conteneur localement pour vérifier que l'application fonctionne correctement.

### Partie 2: Veille Techno

- Lire, analyser et résumer ces trois articles:
    - https://www.softfluent.fr/blog/microservices/
    - https://datamyte.com/blogs/infrastructure-scaling/
    - https://www.redhat.com/en/blog/cloud-vs-on-premises

### Partie 3 : Déploiement sur AWS avec Fargate

#### Préparation de l'Environnement AWS :
Création de l’environnement et d’un VPC pour votre projet.

#### Création d'un Cluster ECS :
- Utiliser Amazon ECS ou Fargate pour créer un cluster.
- Définir une Task Definition avec les paramètres suivants :
    - Image Docker (téléchargée sur Amazon ECR ou Docker Hub).
    - Nombre de conteneurs à exécuter et allocation des ressources (CPU, mémoire).
    - Configuration des variables d'environnement nécessaires.

#### Déploiement de l'Application :
- Déployer la Task dans le cluster ECS.
- Configurer un service ECS pour gérer la disponibilité de l'application (scaling, détection de panne).

#### Configuration du Load Balancer (ALB) :
- Créer une Application Load Balancer (ALB) et configurer les règles d'écoute.
- Associer le service ECS à l'ALB pour gérer le trafic vers les conteneurs



### Partie 4 : Mise en Place de la Sécurité et des Groupes de Droits

#### Création des Security Groups :
Configurer un security group pour le service ECS, limitant l'accès aux seuls ports nécessaires (par exemple, 80 pour HTTP ou 443 pour HTTPS).



## Livrables :
Le Dockerfile et tout autre fichier de configuration nécessaire.
Les captures d'écran ou les liens prouvant le bon fonctionnement de l'application déployée sur AWS.
Un document décrivant les différentes étapes suivies, les défis rencontrés et les solutions apportées.
