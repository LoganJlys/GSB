README - Application de gestion des médecins et rapports
Description du projet
Cette application permet aux utilisateurs d'une entreprise de se connecter à un système sécurisé et de gérer les médecins ainsi que les rapports associés via une interface utilisateur simple et fonctionnelle. Elle repose sur une architecture API et base de données, permettant des interactions rapides et sécurisées. L'interface utilisateur est développée avec Vue.js, tandis que la base de données et les serveurs sont gérés via Docker.

Fonctionnalités principales
Authentification sécurisée : les utilisateurs peuvent se connecter avec leurs identifiants.
Gestion des médecins : ajouter, modifier ou supprimer des informations sur les médecins.
Gestion des rapports : création et suivi des rapports concernant les médecins.
Architecture API pour les échanges de données entre l'interface Vue.js et la base de données.
Structure du projet
Le projet est développé avec Vue.js pour le front-end et s'appuie sur une API pour gérer les échanges de données avec une base de données administrée via PHPMyAdmin. L'ensemble de l'infrastructure est orchestré via Docker.

Principales composantes :
Front-End : Vue.js
Back-End : API (déployée dans Docker)
Base de données : Gérée via PHPMyAdmin et MySQL (dans un conteneur Docker)
Infrastructure : Docker pour le déploiement des services
Configuration et installation
Prérequis
Docker : pour la gestion des conteneurs (API, Base de données)
VS Code : pour le développement et l'édition du code
PHPMyAdmin : pour la gestion et l'administration de la base de données MySQL
Node.js et npm : pour le développement avec Vue.js
Postman (optionnel) : pour tester l'API
Installation
Cloner ce dépôt GitHub :

bash
Copier le code
git clone https://github.com/votre-depot/application-gestion-medecins.git
Configuration de Docker :

Utilisez Docker pour lancer les services nécessaires (API, base de données, PHPMyAdmin).
À partir du fichier docker-compose.yml inclus dans le projet, exécutez la commande :
bash
Copier le code
docker-compose up -d
Cela lancera l'API, le serveur MySQL ainsi que l'interface PHPMyAdmin pour gérer la base de données.
Configurer la base de données :

Accédez à PHPMyAdmin via http://localhost:8080.
Importez le fichier de configuration SQL pour initialiser la base de données des médecins et rapports.
Installer les dépendances front-end :

Allez dans le répertoire du projet Vue.js :
bash
Copier le code
cd frontend
Installez les dépendances :
bash
Copier le code
npm install
Lancer l'application front-end :

Toujours dans le répertoire frontend, démarrez l'application Vue.js :
bash
Copier le code
npm run serve
L'application sera disponible à l'adresse http://localhost:8081.
API
L'API gère les interactions entre l'interface utilisateur et la base de données. Elle est exposée via Docker et repose sur les endpoints suivants :

GET /api/medecins : Récupérer la liste des médecins.
POST /api/medecins : Ajouter un nouveau médecin.
PUT /api/medecins/{id} : Modifier les informations d'un médecin.
DELETE /api/medecins/{id} : Supprimer un médecin.
GET /api/rapports : Récupérer la liste des rapports.
POST /api/rapports : Ajouter un rapport.
PUT /api/rapports/{id} : Modifier un rapport.
DELETE /api/rapports/{id} : Supprimer un rapport.
Utilisation
Une fois l'application configurée et lancée, voici les étapes d'utilisation :

Connexion : Les utilisateurs peuvent se connecter via un formulaire de connexion sécurisé.
Gestion des médecins :
Ajoutez, modifiez ou supprimez des médecins à partir de l'interface.
Les données sont automatiquement synchronisées avec la base de données via l'API.
Gestion des rapports :
Créez ou modifiez des rapports pour les médecins.
Suivez et archivez les rapports directement depuis l'application.
Administration de la base de données :
Utilisez PHPMyAdmin pour effectuer des opérations directement sur la base de données si nécessaire.
Ressources utilisées
Outils logiciels
Docker : Gestion des conteneurs (API, base de données, PHPMyAdmin)
VS Code : Environnement de développement principal
PHPMyAdmin : Outil d'administration pour la base de données MySQL
Vue.js : Framework JavaScript pour le développement de l'interface utilisateur
Documentation
Documentation Docker : https://docs.docker.com/
Documentation Vue.js : https://vuejs.org/
Documentation PHPMyAdmin : https://www.phpmyadmin.net/
