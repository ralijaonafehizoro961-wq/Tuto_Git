# Documentation Tuto git 

Ce dépôt contient les commandes essentielles pour apprendre à utiliser Git et héberger ses projets sur GitHub.

---
## Initialisation d'un projet

Pour commencer à suivre les modifications d'un dossier avec Git :

```bash
# Initialiser le dépôt local
git init

# Connecter le dépôt local à un dépôt distant (GitHub)
git remote add origin [https://github.com/votre-utilisateur/votre-repo.git]

# Vérifier la connexion
git remote -v
```
## Vérifier l'état des fichiers

Avant de faire des modifications, vérifiez l'état de votre dépôt :

```bash
# Voir l'état des fichiers (modifiés, ajoutés, etc.)
git status

# Voir les différences entre les fichiers actuels et la dernière version committée
git diff

# Voir l'historique des commits
git log --oneline
```

## Ajouter des fichiers à l'index (staging)

Pour préparer les fichiers à être committés :

```bash
# Ajouter un fichier spécifique
git add nom_du_fichier

# Ajouter tous les fichiers modifiés
git add .

# Ajouter tous les fichiers (nouveaux, modifiés, supprimés)
git add -A
```

## Commiter les changements

Une fois les fichiers ajoutés, créez un commit :

```bash
# Commiter avec un message
git commit -m "Message descriptif du commit"

# Commiter en incluant tous les fichiers modifiés (sans git add préalable)
git commit -a -m "Message du commit"
```

## Pousser vers le dépôt distant

Envoyez vos commits vers GitHub :

```bash
# Pousser la branche principale
git push origin main

# Pousser une branche spécifique
git push origin nom_de_la_branche
```

## Tirer les changements

Récupérez les changements du dépôt distant :

```bash
# Tirer et fusionner les changements
git pull origin main

# Tirer sans fusionner (fetch seulement)
git fetch origin
```
## Travailler avec les branches

Les branches permettent de travailler sur des fonctionnalités séparément :

```bash
# Voir toutes les branches
git branch

# Créer une nouvelle branche
git branch nom_de_la_branche

# Basculer vers une branche
git checkout nom_de_la_branche

# Créer et basculer vers une nouvelle branche en une commande
git checkout -b nom_de_la_branche

# Supprimer une branche locale
git branch -d nom_de_la_branche
```

## Fusionner des branches

Intégrez les changements d'une branche dans une autre :

```bash
# Fusionner une branche dans la branche actuelle
git merge nom_de_la_branche

# Rebaser pour une histoire linéaire
git rebase nom_de_la_branche
```

## Résoudre les conflits

En cas de conflits lors d'une fusion :

1. Ouvrez les fichiers en conflit
2. Modifiez-les pour résoudre les conflits (supprimez les marqueurs `<<<<<<<`, `=======`, `>>>>>>>`)
3. Ajoutez les fichiers résolus : `git add fichier_en_conflit`
4. Commitez : `git commit`

## Annuler des changements

Pour annuler des modifications :

```bash
# Annuler les changements dans un fichier (revenir à la dernière version committée)
git checkout -- nom_du_fichier

# Annuler le dernier commit (garder les changements)
git reset --soft HEAD~1

# Annuler le dernier commit (supprimer les changements)
git reset --hard HEAD~1

# Annuler un commit spécifique et tous les suivants
git reset --hard commit_hash
```