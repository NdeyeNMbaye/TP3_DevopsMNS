# TD3 - Déploiement d'une Application 3 Tiers avec Vagrant
## Description
Ce projet consiste à déployer une application web en architecture 3 tiers en utilisant Vagrant et VirtualBox. Il s'agit de créer 3 machines virtuelles, d'y déployer une base de données PostgreSQL, un backend Spring Boot et un frontend Angular servi via Nginx.
Les projets déployés sont :

## Backend : ExamJavaM1GL — application Spring Boot de gestion des Classes et Secteurs avec une API RESTful
## Frontend : front-Spring — application Angular qui consomme l'API via un proxy Nginx
## Prérequis

VirtualBox >= 6.1
Vagrant >= 2.3
Git
Contenu du Vagrantfile
Le Vagrantfile définit 3 machines virtuelles :
server-dba (192.168.56.12)

Box : ubuntu/bionic64
Installe PostgreSQL
Crée la base de données et l'utilisateur pour l'application

server-back (192.168.56.11)

Box : ubuntu/bionic64
Installe JDK 17 et Maven
Clone et compile le projet ExamJavaM1GL
Lance l'application Spring Boot comme service systemd sur le port 8080

## server-front (192.168.56.10)

Box : ubuntu/focal64
Installation et Démarrage
## 1. Cloner le projet
bashgit clone https://github.com/NdeyeNMbaye/TP3_DevopsMNS.git
cd TP3_DevopsMNS
## 2. Démarrer toutes les VMs
   vagrant up

Le premier démarrage peut prendre des minutes.
## Démarrage des VMs
<img width="1275" height="801" alt="image" src="https://github.com/user-attachments/assets/1e3b9f4d-6d1c-41d6-b7b6-16b0c5fb3800" />
<img width="836" height="266" alt="image" src="https://github.com/user-attachments/assets/c89d5faf-a39f-4858-975a-5a333eab47c1" />
-SECTEURS 
<img width="1917" height="544" alt="image" src="https://github.com/user-attachments/assets/331017d5-3590-4be0-9e68-7e2c8143f953" />
<img width="1919" height="854" alt="image" src="https://github.com/user-attachments/assets/bfee23e4-d882-4010-98be-9f892f16dd0b" />
-CLASSES 
<img width="1918" height="709" alt="image" src="https://github.com/user-attachments/assets/cd3203b2-4297-4612-8345-f58a42a25d2d" />
-Ajouter une classe 
<img width="1663" height="527" alt="image" src="https://github.com/user-attachments/assets/fd41f749-b42e-4cf8-9ea8-9ab18d42fedc" />






Installe Node.js 18, Angular CLI et Nginx
Clone et compile le projet front-Spring
Configure Nginx comme reverse proxy vers server-back avec gestion CORS
