# Repository BobApp CI/CD 

## Lien du repository GitHub

https://github.com/bem92/APP-CI-CD

## Workflows GitHub Actions implémentés

Le repository contient une pipeline CI/CD complète avec :

### 1. Workflow CI/CD
Pipeline complète qui exécute les tests, vérifie la qualité et déploie sur Docker Hub

### 2. Workflow des tests  
- Tests backend avec Maven et génération rapport JaCoCo
- Tests frontend avec Karma et génération rapport LCOV

### 3. Workflow de qualité
- Analyse SonarCloud pour backend et frontend
- Vérification du Quality Gate

## Principe de conditionnement

**Chaque étape du workflow doit être validée avec succès avant de passer à la suivante**. Le déploiement sur Docker Hub est réalisé **si et seulement si** toutes les étapes précédentes ont réussi (tests + qualité).

## Images Docker Hub

Les images Docker validées sont publiées sur :
- **Backend** : `docker.io/nejrima/projet10:back-latest` (branche main) / `docker.io/nejrima/projet10:back-dev` (branche dev)
- **Frontend** : `docker.io/nejrima/projet10:front-latest` (branche main) / `docker.io/nejrima/projet10:front-dev` (branche dev)

## Dashboards SonarCloud

- Organisation : **bem92**
- Projet Backend : **back-app**
- Projet Frontend : **front-app**

URL : https://sonarcloud.io/organizations/bem92/projects

## Note importante

Le plan gratuit de SonarCloud ne permet pas de créer des Quality Gates personnalisées.
