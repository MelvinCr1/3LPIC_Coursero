# Projet Coursero – Correction Automatique d’Exercices (PoC)
![Status](https://img.shields.io/badge/Status-PoC_%2F_Prototype-orange?style=flat-square)
![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)
![Version](https://img.shields.io/badge/Version-1.0.0-green?style=flat-square)

> **Plateforme web éducative permettant le dépôt, le suivi et l'évaluation automatique d'exercices de programmation.**

---

## 📑 Sommaire
1. [Contexte du projet](#-1-contexte-du-projet)
2. [Fonctionnalités](#-2-fonctionnalités)
3. [Stack Technique](#-3-stack-technique)
4. [Installation & Configuration](#-4-installation--configuration)
5. [Auteurs](#-5-auteurs)

## 📝 1. Contexte du projet

Plateforme web permettant aux étudiants de déposer, suivre et évaluer automatiquement des exercices de programmation.

**Objectifs principaux :**
* **Interface Étudiant :** Connexion sécurisée et tableau de bord personnel.
* **Gestion de fichiers :** Dépôt centralisé de scripts (Python, C).
* **Archivage :** Stockage structuré des soumissions.
* **Automation :** Base technique pour l'intégration de tests unitaires et corrections automatiques.

---

## 🚀 2. Fonctionnalités

### 2.1 - Gestion des utilisateurs
* Authentification sécurisée (Login/Mot de passe).
* Interface de session pour les étudiants.

### 2.2 - Dépôt de fichiers
* Envoi d’exercices au format .py, .c, etc.
* Organisation des fichiers par étudiant et par exercice.

### 2.3 - Suivi des soumissions
* Historique des envois.
* Horodatage (Timestamp) des dépôts.
* Statut d'évaluation en temps réel.

### 2.4 - Moteur de correction
* Architecture modulaire pour l'exécution de scripts de tests.
* Sandboxing (via VM) pour la compilation et l'exécution sécurisée.
* Retour visuel du résultat (Succès/Échec).

---

## 🛠 3. Stack Technique

### Frontend
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

### Backend & Database
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-005C84?style=for-the-badge&logo=mysql&logoColor=white)

### Langages supportés (Exercices)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)

### Infrastructure
![VMware](https://img.shields.io/badge/VMware-607078?style=for-the-badge&logo=vmware&logoColor=white)

---

## 💻 4. Installation & Configuration

### 4.1 - Prérequis
* **Virtualisation :** VMware Workstation Pro (ou équivalent).
* **Serveur Web :** Apache/Nginx avec PHP ≥ 7.4.
* **Base de données :** MySQL ou MariaDB.

### 4.2 Configuration des VMs
Le projet repose sur une architecture virtualisée. Téléchargez les images disques ici :

[📥 Télécharger les VMs (MEGA)](https://mega.nz/folder/6d9Akb4D#rMqQIehODLRE7Faj2DKcpw)

> [!WARNING]
> **Configuration Réseau :**
> Assurez-vous que les VMs sont sur le même réseau virtuel (NAT ou Bridged). Vous devrez probablement modifier les adresses IP statiques dans les fichiers de configuration système pour correspondre à votre sous-réseau local.

### 4.3 Déploiement

1.  **Cloner le dépôt :**
    ```bash
    git clone [https://github.com/MelvinCr1/3LPIC_Coursero.git](https://github.com/MelvinCr1/3LPIC_Coursero.git)
    cd 3LPIC_Coursero
    ```

2.  **Base de données :**
    * Créez une base de données MySQL.
    * Importez le schéma via le fichier `config.sql` fourni à la racine.

3.  **Configuration :**
    * Renommez `config.example.php` en `config.php` (si applicable).
    * Modifiez les identifiants de la BDD :
    ```php
    // config.php
    $db_host = 'localhost';
    $db_name = 'coursero_db';
    $db_user = 'root';
    $db_pass = 'votre_mot_de_passe';
    ```

4.  **Lancement :**
    * Démarrez votre serveur local (WAMP/XAMPP/MAMP ou service Linux).
    * Accédez à : `http://localhost/coursero/`.

### 4.4 Création d'un compte (Test)
L'inscription est ouverte pour le PoC.
1.  Rendez-vous sur `/register.php`.
2.  Créez un compte étudiant.
3.  Connectez-vous pour accéder au dashboard.

---

## 5. Authors

* **Melvin Cureau** - *Développeur Principal* - [@MelvinCr1](https://github.com/MelvinCr1)
---

## 6. Licence

Ce projet est sous licence **MIT**. Consultez le fichier [LICENSE](LICENSE) pour plus de détails.
