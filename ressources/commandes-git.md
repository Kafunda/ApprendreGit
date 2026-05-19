# Commandes Git Essentielles 🚀

Ce document regroupe les principales commandes Git à connaître pour travailler efficacement sur vos projets.

---

# 📦 Initialisation du dépôt

## Initialiser un dépôt Git

```bash
git init
```

Transforme le dossier courant en dépôt Git.

---

# 👤 Configuration Git

## Configurer le nom d’utilisateur

```bash
git config --global user.name "Votre Nom"
```

## Configurer l’email

```bash
git config --global user.email "votre@email.com"
```

## Afficher la configuration

```bash
git config --global user.name
git config --global user.email
```

---

# 📄 Vérifier l’état du projet

## Voir l’état du dépôt

```bash
git status
```

Permet de voir :

- les fichiers modifiés ;
- les fichiers non suivis ;
- les fichiers prêts pour le commit.

---

# ➕ Ajouter des fichiers

## Ajouter un fichier spécifique

```bash
git add index.html
```

---

## Ajouter tous les fichiers

```bash
git add .
```

---

# 💾 Sauvegarder les modifications

## Créer un commit

```bash
git commit -m "Mon message"
```

---

# 📜 Historique des commits

## Voir tous les commits

```bash
git log
```

---

## Affichage compact

```bash
git log --oneline
```

---

## Affichage graphique

```bash
git log --oneline --graph --decorate
```

---

# 🌿 Gestion des branches

## Afficher les branches

```bash
git branch
```

---

## Créer une branche

```bash
git branch nom-branche
```

---

## Changer de branche

```bash
git switch nom-branche
```

ou

```bash
git checkout nom-branche
```

---

## Créer et changer de branche directement

```bash
git switch -c nom-branche
```

ou

```bash
git checkout -b nom-branche
```

---

## Supprimer une branche

```bash
git branch -d nom-branche
```

---

# 🔀 Fusion des branches

## Fusionner une branche

```bash
git merge nom-branche
```

Fusionne la branche indiquée dans la branche actuelle.

---

# ☁️ GitHub et dépôt distant

## Ajouter un dépôt distant

```bash
git remote add origin URL_DU_REPO
```

---

## Envoyer le projet vers GitHub

```bash
git push -u origin main
```

---

## Envoyer une branche

```bash
git push -u origin nom-branche
```

---

## Récupérer les modifications distantes

```bash
git pull
```

---

## Cloner un dépôt

```bash
git clone URL_DU_REPO
```

---

# ⏪ Revenir en arrière

## Retirer un fichier du staging

```bash
git reset nom-fichier
```

---

## Reset soft

```bash
git reset --soft ID_COMMIT
```

Annule les commits sans supprimer les modifications.

---

## Reset mixed

```bash
git reset --mixed ID_COMMIT
```

Annule les commits et retire les fichiers du staging.

---

## Reset hard

⚠️ Attention : suppression définitive des modifications.

```bash
git reset --hard ID_COMMIT
```

---

# 🛠️ Modifier le dernier commit

## Ajouter des modifications au dernier commit

```bash
git commit --amend --no-edit
```

---

# 🔍 Historique avancé

## Voir toutes les actions Git

```bash
git reflog
```

---

## Voir l’auteur de chaque ligne

```bash
git blame nom-fichier
```

---

# 🚫 Ignorer des fichiers

## Créer un fichier .gitignore

```bash
touch .gitignore
```

Exemple :

```gitignore
node_modules/
.env
__pycache__/
```

---

# 🔥 Workflow Git classique

```bash
git init
git status
git add .
git commit -m "Premier commit"

git branch feature-login
git switch feature-login

git add .
git commit -m "Ajout du login"

git switch main
git merge feature-login

git push
```

---

# ✅ Bonnes pratiques

- Faire des commits fréquents
- Utiliser des messages clairs
- Créer une branche par fonctionnalité
- Vérifier régulièrement `git status`
- Utiliser `git log` pour suivre l’historique

---

# 📖 Ressources utiles

- https://git-scm.com/doc
- https://docs.github.com
- https://skills.github.com

---

⭐ Continuez à pratiquer Git régulièrement !