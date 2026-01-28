# Module 4 : Outils Avancés

Quand on maîtrise les bases, Git offre des outils puissants pour nettoyer son historique ou gérer des situations complexes.

## 🎯 Objectifs
- Utiliser `stash` pour mettre de côté le travail.
- "Picorer" des commits avec `cherry-pick`.
- Annuler des actions avec `reset` et `revert`.
- Nettoyer l'historique avec l'interactive rebase.

## 1. Git Stash
Vous devez changer de branche mais vous n'avez pas fini votre travail ? Ne commitez pas du code cassé !

```bash
# Mettre de côté les modifs non commitées
git stash

# Récupérer les modifs plus tard (sur n'importe quelle branche)
git stash pop
```

## 2. Cherry-Pick
Permet de prendre un commit spécifique d'une autre branche et de l'appliquer sur votre branche actuelle.

```bash
git cherry-pick <commit-hash>
```
*Utile pour hotfixer un bug en production sans fusionner toute une branche de développement.*

## 3. Annuler des Changements

### `git revert` (Safe)
Crée un *nouveau* commit qui fait l'inverse du commit précédent. C'est la méthode sûre pour annuler un commit public.
```bash
git revert <commit-hash>
```

### `git reset` (Destructif)
Revient en arrière dans l'histoire.
-   `git reset --soft` : Garde vos changements dans le staging area.
-   `git reset --hard` : **Supprime** tous les changements. Danger !

```bash
# Annuler le dernier commit mais garder les fichiers
git reset --soft HEAD~1
```

## 4. Interactive Rebase
Pour nettoyer votre historique local avant de push (fusionner des commits, changer les messages...).

```bash
git rebase -i HEAD~3
```
Cela ouvre un éditeur où vous pouvez choisir `pick`, `squash` (fusionner), `reword` (renommer), etc.

---
[Précédent](../03_Travail_Collaboratif/README.md) | [Retour au sommaire](../README.md) | [Suivant : Module 5](../05_Projets_Pratiques/README.md)
