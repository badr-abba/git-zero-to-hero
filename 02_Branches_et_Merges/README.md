# Module 2 : Branches et Merges

Les branches sont au cœur de la puissance de Git, permettant de travailler sur plusieurs fonctionnalités en parallèle sans impacter le code principal.

## 🎯 Objectifs
- Comprendre et manipuler les branches.
- Maîtriser le fusionnement (`merge`).
- Gérer les conflits de fusion.

## 1. Pourquoi les Branches ?
Une branche est une ligne de développement indépendante. La branche par défaut s'appelle généralement `main` (ou `master`). Créer une branche permet de développer une fonctionnalité, corriger un bug ou tester une idée sans "casser" la version stable.

## 2. Commandes de Base

### Créer et Changer de branche
```bash
# Créer une branche
git branch feature-login

# Basculer dessus
git checkout feature-login

# Raccourci (Créer + Basculer)
git checkout -b feature-dashboard
```
*(Note : Sur les versions récentes de Git, `git switch` remplace `git checkout` pour changer de branche)*

### Lister et Supprimer
```bash
# Lister les branches
git branch

# Supprimer une branche (une fois fusionnée)
git branch -d feature-login
```

## 3. Fusionner (Merge)
Une fois votre travail terminé sur une branche, vous devez le ramener dans `main`.

```bash
git checkout main
git merge feature-dashboard
```

## 4. Gestion des Conflits
Un conflit survient quand Git ne peut pas décider automatiquement quelles modifications garder (ex: deux personnes ont modifié la même ligne).

**Procédure de résolution :**
1.  Git vous avertit du conflit lors du merge.
2.  Ouvrez les fichiers conflictuels.
3.  Recherchez les marqueurs `<<<<<<<`, `=======`, `>>>>>>>`.
4.  Éditez le fichier pour garder la version souhaitée.
5.  Ajoutez le fichier résolu (`git add`).
6.  Terminez le merge (`git commit`).

---
[Précédent](../01_Introduction/README.md) | [Retour au sommaire](../README.md) | [Suivant : Module 3](../03_Travail_Collaboratif/README.md)
