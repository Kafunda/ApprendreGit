# Exercice 1 : Initialiser un projet et faire des commits 🚀

## 🎯 Objectif
Dans cet exercice, vous allez apprendre à :

- Initialiser un dépôt Git
- Vérifier l’état du dépôt
- Ajouter des fichiers dans la Staging Area
- Créer plusieurs commits

---

## 📌 Consignes

### 1. Créer un dossier de projet
Créez un dossier nommé :

```bash
mon_projet_git
```

---

### 2. Initialiser Git

Initialisez un dépôt Git dans ce dossier.

📌 Question :
- Quelle commande permet d’initialiser un dépôt Git ?

---

### 3. Vérifier l’état du dépôt

Affichez l’état actuel du dépôt.

📌 Question :
- Quelle commande permet de voir les fichiers suivis ou non suivis ?

---

### 4. Créer un fichier

Créez un fichier nommé :

```bash
index.html
```

Ajoutez-y le contenu suivant :

```html
<h1>Bonjour Git</h1>
```

---

### 5. Ajouter le fichier à la Staging Area

Ajoutez `index.html` dans la zone de staging.

📌 Question :
- Quelle commande permet d’ajouter un fichier au staging ?

---

### 6. Faire un premier commit

Effectuez un commit avec le message :

```bash
Premier commit
```

📌 Question :
- Quelle commande permet de créer un commit ?

---

### 7. Modifier le fichier

Ajoutez cette ligne dans `index.html` :

```html
<p>Bienvenue dans Git</p>
```

---

### 8. Vérifier les modifications

Affichez à nouveau l’état du dépôt.

📌 Question :
- Que remarquez-vous après modification du fichier ?

---

### 9. Ajouter et commit les modifications

Ajoutez les modifications puis créez un nouveau commit avec le message :

```bash
Ajout du paragraphe de bienvenue
```

---

## ✅ Résultat attendu

À la fin de cet exercice :

- votre projet doit être un dépôt Git ;
- le fichier `index.html` doit être suivi par Git ;
- vous devez avoir au moins 2 commits.

---

---

# 🔥 Bonus avancé

## 1. Vérifier l’historique des commits

Affichez l’historique du projet avec :

```bash
git log
```

Puis essayez :

```bash
git log --oneline --graph --decorate
```

📌 Questions :
- Quelle différence observez-vous entre les deux affichages ?
- Quel affichage est le plus lisible ?

---

## 2. Modifier le dernier commit

Ajoutez une nouvelle ligne dans `index.html` :

```html
<footer>Mon footer</footer>
```

Ajoutez le fichier dans le staging puis fusionnez les modifications avec le commit précédent sans créer un nouveau commit.

📌 Question :
- Quelle commande permet de modifier le dernier commit ?

---

## 3. Tester git reset

Créez un nouveau fichier :

```bash
test.txt
```

Ajoutez-le dans le staging.

Ensuite retirez-le du staging avec :

```bash
git reset
```

📌 Questions :
- Le fichier a-t-il été supprimé ?
- Que fait réellement `git reset` dans ce cas ?

---