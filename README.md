## Formation : Apprendre les bases de Git et GitHub


Bienvenue dans ce dépôt dédié à l’apprentissage des bases de Git et GitHub.  
Ce guide est conçu pour les débutants qui souhaitent comprendre le fonctionnement du contrôle de version et apprendre à collaborer efficacement sur des projets de développement.

---

## 📚 Contenu de la formation

Dans cette formation, vous apprendrez :

- Comprendre la différence entre **Git** et **GitHub**
- Installer et configurer Git
- Créer et gérer un dépôt (*repository*)
- Utiliser les commandes essentielles de Git
- Comprendre le cycle de vie d’un projet Git
- Créer et gérer des branches
- Fusionner des branches avec `merge`
- Envoyer un projet sur GitHub

---

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
### Installer et configurer Git et Github

# Configuration de Git et GitHub

Ce guide rapide vous explique comment installer Git sur votre machine et configurer vos identifiants pour commencer à suivre vos projets avec GitHub.

---

## 1. Télécharger et installer Git

1. Rendez-vous sur le site officiel [git-scm.com](https://git-scm.com/) pour télécharger le fichier d'installation adapté à votre système d'exploitation.
2. Lancez l'assistant d'installation.

> 💡 **Note importante :** Lors de l'installation, veillez à laisser cochée l'option qui propose d'ajouter Git aux **variables d'environnement** (généralement activée par défaut). Cela vous permettra d'utiliser les commandes Git depuis n'importe quel terminal.

### Vérification de l'installation
Une fois l'installation terminée, ouvrez un terminal :
* **Sur Windows :** Appuyez sur les touches `Win + R`, tapez `cmd` ou `powershell`, puis validez.
* **Sur macOS / Linux :** Ouvrez votre application Terminal.

Entrez la commande suivante pour vérifier que Git est bien installé :
```bash
git --version

```

3. aller sur  sur www.Github.com et creer votre compte  
   
4. configurer l'utilisateur git : 
il y a deux type de configuration, global et local
* **`global`** : Ces identifiants s'appliqueront par défaut à tous vos projets sur votre machine. C'est l'option recommandée pour votre ordinateur personnel.
**`git config --global user.name "votre nom"`**
**`git config --global user.email "votre email"`**
pour voir les infos de votre config : 
**`git config --global user.name`**
**`git config --global user.email`**
* **`local`** : Cette configuration s'applique uniquement au projet courant (dans le dossier où vous vous trouvez). Elle est très utile si vous devez utiliser un compte professionnel pour certains projets et un compte personnel pour d'autres.
**`git config --local user.name "Votre Nom Spécifique"`**
**`git config --local user.email "votre.email.specifique@exemple.com"`**
pour voir les infos de votre config : 
**`git config --local user.name`**
**`git config --local user.email`**

---
### Les commandes de base


* **`git init`** : Cette commande initialise un nouveau dépôt Git dans ton dossier de projet (*Working Directory* ou Espace de travail). C'est elle qui dit à Git de commencer à surveiller ce dossier.
* **`git add`** : Elle permet d'indexer tes fichiers en les plaçant dans un espace temporaire appelé la **Staging Area** (zone de transit). Elle prépare tes fichiers avant de les valider définitivement dans le dépôt.
    * *Exemple :* `git add index.html` 
* **`git commit`** : Elle permet d'enregistrer définitivement tes fichiers indexés dans le dépôt local après validation, en créant un point dans l'historique (un snapshot).
    * *Exemple :* `git commit -m "message sur la tache effectuer"`
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

### Créer et gérer une branche
Par défaut, Git crée une branche principale nommée **`main`** (ou historiquement **`master`**). 



Il est vivement conseillé de créer une branche distincte pour chaque nouvelle fonctionnalité ou correction de bug. Ainsi, en cas de problème, tu ne risques pas de casser le projet principal.

* **`git branch <nom_de_la_branche>`** : Crée une nouvelle branche à partir de la branche où tu te trouves, sans pour autant basculer dessus.
  * *Exemple :* `git branch recherche` (crée la branche dédiée à la fonctionnalité de recherche).
* **`git checkout <nom_de_la_branche>`** ou **`git switch <nom_de_la_branche>`** : Permet de basculer sur la branche spécifiée pour commencer à y travailler.
  * *Exemple :* `git switch recherche`
* **`git checkout -b <nom_de_la_branche>`** ou **`git switch -c <nom_de_la_branche>`** : Combine la création et le basculement immédiat sur la nouvelle branche en une seule commande. *(Attention : la syntaxe exacte est `git checkout -b` et non `git branch -b`)*.
  * *Exemple :* `git checkout -b recherche`
* **`git push -u origin <nom_de_la_branche>`** : Permet d'envoyer ta nouvelle branche locale pour la première fois vers le dépôt distant (GitHub) et de lier les deux. Les fois suivantes, un simple `git push` suffira.
  * *Exemple :* `git push -u origin recherche`

---

### Fusionner une branche (Merge)
Après avoir terminé le développement et validé tes modifications (via des commits) sur ta branche secondaire, il faut la fusionner avec la branche principale pour intégrer tes nouveautés au projet global.

Pour effectuer une fusion, tu dois obligatoirement **te placer d'abord sur la branche qui va recevoir les modifications** (généralement `main`).

1. Reviens sur la branche principale :
   ```bash
   git switch main
* **`git merge <nom_de_la_branche> `**
    * *Exemple :* `git merge recherche`.

## Revenir sur les versions précédentes de votre projet

Il se peut que vous ayez besoin de revenir en arrière pour retrouver une ancienne fonctionnalité de votre projet. Pas de panique, Git a tout prévu avec la commande `git reset`.

Il existe 3 types de reset selon ce que vous souhaitez conserver ou annuler :

### 1. Le mode Soft (`--soft`)
Permet de revenir en arrière en annulant les commits, **sans supprimer aucun fichier ni aucune modification**. Vos changements récents sont conservés et placés directement dans la zone de staging (prêts à être commités à nouveau).
```bash
git reset --soft <ID_DU_COMMIT>

```

### 2. Le mode mixed (`--mixed`)
C'est le comportement par défaut de Git si vous ne précisez rien. Il annule les commits et sort les modifications de la zone de staging. Vos fichiers restent inchangés sur votre disque dur, mais vos modifications récentes apparaissent comme "non suivies" (not staged).
```bash
git reset --mixed <ID_DU_COMMIT>

```
### 3. Le mode hard (`--hard`)
Attention : Cette action est destructive et irréversible.
Le mode hard permet de revenir en arrière en supprimant définitivement tous les fichiers et toutes les modifications créés après le commit cible. Votre projet revient exactement dans l'état où il était à ce moment-là.
```bash
git reset --hard <ID_DU_COMMIT>

```

---

# 📖 Ressources utiles

- Documentation officielle Git : https://git-scm.com/doc
- Documentation GitHub Docs : https://docs.github.com
- GitHub Skills : https://skills.github.com

---

⭐ N'hésitez pas à laisser une étoile au dépôt si ce guide vous aide !
