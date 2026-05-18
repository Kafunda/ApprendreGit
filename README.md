## Formation : Apprendre les bases de Git et GitHub

Dans cette formation, nous allons explorer les fondamentaux de Git et GitHub, deux outils incontournables pour tout développeur moderne.

### 1. GitHub : Ton code dans le Cloud
Vois GitHub comme une plateforme en ligne (un site web) qui héberge et stocke ton code source. Il permet de centraliser tes projets, de collaborer facilement en équipe et de partager ton travail avec le monde entier.

### 2. Git : Le gardien de ton historique
Git est un logiciel de gestion de versions (VCS) installé localement sur ta machine. Il fonctionne comme une machine à remonter le temps : il t'aide à sauvegarder les différentes versions de ton code à l'aide du controle de version. Grâce à lui, tu peux tester de nouvelles fonctionnalités sans risquer de casser ce qui fonctionne déjà, et revenir en arrière à tout moment.

---

### Le concept de Dépôt (Repository)
Git et GitHub enregistrent tes modifications au sein d'un dépôt (souvent appelé "Repo"). Tu peux imaginer le dépôt comme un coffre-fort numérique ou une archive intelligente qui contient l'intégralité des fichiers de ton projet, ainsi que tout l'historique de ses modifications.

Il existe deux types de dépôts :

* **Le dépôt privé :** Seules les personnes explicitement autorisées par toi peuvent voir le code, y accéder et modifier le projet. C'est idéal pour les projets commerciaux ou confidentiels.
* **Le dépôt public :** Tout le monde sur Internet peut voir ton code et s'en inspirer. Cependant, seules les personnes que tu auras désignées comme collaboratrices pourront modifier directement le projet. Les autres utilisateurs devront te proposer des suggestions de modifications (via ce qu'on appelle des *Pull Requests*). C'est la base du monde de l'Open Source.

---

### Les commandes de base



* **`git init`** : Cette commande initialise un nouveau dépôt Git dans ton dossier de projet (*Working Directory* ou Espace de travail). C'est elle qui dit à Git de commencer à surveiller ce dossier.
* **`git add`** : Elle permet d'indexer tes fichiers en les plaçant dans un espace temporaire appelé la **Staging Area** (zone de transit). Elle prépare tes fichiers avant de les valider définitivement dans le dépôt.
* **`git commit`** : Elle permet d'enregistrer définitivement tes fichiers indexés dans le dépôt local après validation, en créant un point dans l'historique (un snapshot).

---

### Cycle de vie d'un projet Git

Le projet suit cette démarche du moment où il est initialisé :



* **`Working Directory`** (Dossier de travail) : C'est l'espace où tu crées, modifies et supprimes tes fichiers. Ici, Git surveille tes fichiers et toutes les modifications qu'ils subissent.
* **`Staging Area`** (Zone d'indexation) : Tes fichiers y sont placés de manière temporaire. C'est l'antichambre du dépôt, où tu prépares et organises tes modifications en attendant la validation définitive.
* **`Dépôt (Repository)`** : C'est le coffre-fort local situé sur ta machine. Une fois le commit effectué, tes fichiers et leur historique y sont stockés de manière sécurisée.
* **`GitHub`** (Dépôt distant) : Tes fichiers et tout l'historique du projet sont envoyés dans un dépôt distant hébergé dans le Cloud, ce qui permet de sauvegarder ton travail en ligne et de collaborer avec d'autres développeurs.
### Tableau récapitulatif : Concepts clés et Commandes

| Concept / Mot-clé | Action ou Commande Git | Description et Impact |
| :--- | :--- | :--- |
| **Working Directory** <br>*(Espace de travail)* | `git init` | **Création de l'espace :** Initialise un dépôt Git et transforme ton dossier local en un *Working Directory* officiellement surveillé par Git. |
| **Staging Area** <br>*(Zone d'indexation)* | `git add <nom_fichier>` | **Préparation :** Transfère tes fichiers modifiés depuis le *Working Directory* vers la *Staging Area* (zone de transit) pour préparer le prochain commit. |
| **Dépôt Local (Repository)** <br>*(Coffre-fort)* | `git commit -m "Message"` | **Enregistrement :** Valide et fige les modifications de la *Staging Area* dans l'historique de ton dépôt local. |
| **GitHub (Dépôt Distant)** <br>*(Le Cloud)* | `git push` | **Sauvegarde & Partage :** Envoie tous les commits de ton dépôt local vers ton dépôt distant sur GitHub. |