# Module 5 : Projets Pratiques

Mettez en pratique vos connaissances avec des simulations de scénarios réels.

## 🎯 Objectifs
- Simuler un conflit d'équipe.
- Mettre en place un pipeline CI/CD simple.

## 1. Simulation : Le Conflit de Fusion
Pour cet exercice, vous allez jouer deux rôles : le **Développeur A** et le **Développeur B**.

1.  Créez un dépôt et un fichier `main.txt` avec la ligne "Version 1".
2.  **Dev A** crée une branche `feature-a`, change la ligne en "Version A", commit.
3.  **Dev B** (revenez sur `main`) crée une branche `feature-b`, change la ligne en "Version B", commit.
4.  Fusionnez `feature-a` dans `main`. (Succès).
5.  Tentez de fusionner `feature-b` dans `main`. **CONFLIT !**
6.  Résolvez le conflit pour garder les deux versions ou une combinaison.

## 2. Introduction au CI/CD avec GitHub Actions
L'Intégration Continue (CI) permet de tester votre code automatiquement à chaque push.

1.  Sur votre dépôt GitHub, allez dans l'onglet **Actions**.
2.  Choisissez "Simple workflow".
3.  GitHub crée un fichier `.github/workflows/blank.yml`.

Voici un exemple simple qui affiche "Hello World" à chaque push :

```yaml
name: CI Demo
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Run a one-line script
        run: echo Hello, World!
```

À chaque fois que vous pousserez du code, GitHub exécutera ce script. C'est la base pour lancer des tests automatiques !

---
[Précédent](../04_Outils_Avances/README.md) | [Retour au sommaire](../README.md)
