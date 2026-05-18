# Exercice 2 : Manipuler les branches Git 🌿

## 🎯 Objectif

Dans cet exercice, vous allez apprendre à :

- Créer des branches
- Changer de branche
- Modifier un projet sur une branche secondaire
- Fusionner une branche avec `main`

---

## 📌 Consignes

### 1. Vérifier votre branche actuelle

Affichez la branche active.

📌 Question :
- Quelle commande permet de voir les branches ?

---

### 2. Créer une branche

Créez une branche nommée :

```bash
feature-navbar
```

📌 Question :
- Quelle commande permet de créer une branche ?

---

### 3. Basculer sur la nouvelle branche

Déplacez-vous sur :

```bash
feature-navbar
```

📌 Question :
- Quelle commande permet de changer de branche ?

---

### 4. Modifier le projet

Dans le fichier `index.html`, ajoutez :

```html
<nav>Menu de navigation</nav>
```

---

### 5. Ajouter et commit les modifications

Ajoutez les modifications puis créez un commit avec le message :

```bash
Ajout de la navbar
```

---

### 6. Revenir sur la branche principale

Revenez sur :

```bash
main
```

📌 Question :
- Le code de la navbar apparaît-il sur `main` avant le merge ?

---

### 7. Fusionner la branche

Fusionnez :

```bash
feature-navbar
```

dans `main`.

📌 Question :
- Quelle commande permet de fusionner une branche ?

---

### 8. Vérifier le résultat

Affichez le contenu de `index.html`.

📌 Question :
- Que remarquez-vous après le merge ?

---

### 9. Supprimer la branche

Supprimez :

```bash
feature-navbar
```

📌 Question :
- Quelle commande permet de supprimer une branche ?

---

## ✅ Résultat attendu

À la fin de cet exercice :

- une branche secondaire doit avoir été créée ;
- les modifications doivent avoir été fusionnées dans `main` ;
- la branche secondaire doit être supprimée.

---

## 🔥 Bonus

1. Affichez l’historique sous forme graphique :

```bash
git log --oneline --graph --decorate
```

2. Essayez de créer une deuxième branche nommée :

```bash
feature-footer
```

et ajoutez un footer au projet.