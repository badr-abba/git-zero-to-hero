# Module 3 : Travail Collaboratif

Git est conçu pour la collaboration. Ce module explique comment interagir avec des dépôts distants (Remotes) et utiliser des plateformes comme GitHub.

## 🎯 Objectifs
- Comprendre la notion de "Remote".
- Pousser (`push`) et récupérer (`pull`) du code.
- Utiliser les Pull Requests pour la revue de code.

## 1. Les Remotes (Dépôts Distants)
Un Remote est une version de votre projet hébergée sur Internet ou un autre réseau. Le remote par défaut s'appelle généralement `origin`.

### Commandes Clés
```bash
# Voir les remotes configurés
git remote -v

# Ajouter un remote
git remote add origin https://github.com/user/repo.git

# Cloner un dépôt existant (configure automatiquement 'origin')
git clone https://github.com/user/repo.git
```

## 2. Push & Pull
Pour synchroniser votre travail :

-   **`git push`** : Envoie vos commits locaux vers le remote.
    ```bash
    git push origin main
    ```
-   **`git pull`** : Récupère les modifications du remote et les fusionne dans votre branche actuelle.
    ```bash
    git pull origin main
    ```

## 3. Pull Requests (PR) & Code Review
Dans un environnement professionnel, on ne pousse jamais directement sur `main`. On utilise des **Pull Requests** (ou Merge Requests sur GitLab).

1.  Poussez votre feature branche : `git push origin feature-login`.
2.  Sur GitHub, ouvrez une Pull Request de `feature-login` vers `main`.
3.  Vos collègues relisent le code ("Code Review"), laissent des commentaires.
4.  Une fois validée, la PR est fusionnée.

## 4. Le Workflow "Fork & Pull"
Pour contribuer à des projets Open Source où vous n'avez pas les droits d'écriture :
1.  **Fork** : Créez une copie du dépôt sur votre compte GitHub.
2.  **Clone** : Clonez votre fork localement.
3.  **Push** : Poussez vos modifs sur votre fork.
4.  **PR** : Faites une Pull Request depuis votre fork vers le dépôt original.

---
[Précédent](../02_Branches_et_Merges/README.md) | [Retour au sommaire](../README.md) | [Suivant : Module 4](../04_Outils_Avances/README.md)
