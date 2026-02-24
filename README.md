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