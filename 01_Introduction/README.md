# Module 1 : Introduction et Configuration

Ce module couvre les bases essentielles de Git, de l'installation à votre premier commit.

## 🎯 Objectifs
- Comprendre les 3 zones de Git.
- Configurer son identité.
- Initialiser un dépôt et faire son premier commit.

## 1. Les Concepts Clés de Git

Git fonctionne avec trois zones principales :

1.  **Working Directory (Répertoire de travail)** : C'est là où vous modifiez vos fichiers actuellement.
2.  **Staging Area (Index)** : Une zone tampon où vous préparez les modifications à valider (avec `git add`).
3.  **Repository (Dépôt local)** : La base de données où Git stocke l'historique de vos versions (avec `git commit`).

## 2. Configuration Globale

Avant de commencer, vous devez dire à Git qui vous êtes. Ces informations apparaissent dans chaque commit.

```bash
git config --global user.name "Votre Nom"
git config --global user.email "votre.email@exemple.com"
```

Vérifier la configuration :
```bash
git config --list
```

## 3. Initialiser un Dépôt

Pour transformer un dossier en dépôt Git :

```bash
mkdir mon_projet_git
cd mon_projet_git
git init
```
Cela crée un dossier caché `.git`.

## 4. Votre Premier Commit

Le cycle de vie classique d'un fichier : **Modifier** -> **Stager** -> **Commiter**.

1.  Créer un fichier :
    ```bash
    echo "# Mon Projet" > README.md
    ```
2.  Ajouter à la Staging Area :
    ```bash
    git add README.md
    ```
3.  Valider (Commit) :
    ```bash
    git commit -m "feat: initial commit avec README"
    ```

> **Astuce** : Utilisez `git status` à tout moment pour voir l'état de vos fichiers.

---
[Retour au sommaire](../README.md) | [Suivant : Module 2](../02_Branches_et_Merges/README.md)
