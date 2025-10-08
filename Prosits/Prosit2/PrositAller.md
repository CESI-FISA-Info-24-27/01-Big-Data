# Prosit 2 - Prosit Aller

## Prendre connaissance de la situation et la clarifier

### Mots inconnus

entrepôt de données, système décisionnel, référentiel de stockage, ETL, HIVE, transformation des données

#### Définitions rapides

1. **Entrepôt de données** : Un entrepôt de données est une base de données centralisée qui stocke des données provenant de diverses sources, organisées pour l'analyse et la génération de rapports.

2. **Système décisionnel** : Un système décisionnel est un ensemble d'outils, de technologies et de processus qui aident les entreprises à prendre des décisions basées sur des données et des analyses.

3. **Référentiel de stockage** : Un référentiel de stockage est un emplacement centralisé où les données sont stockées, organisées et gérées pour une utilisation ultérieure.

4. **ETL (Extract, Transform, Load)** : ETL est un processus en trois étapes utilisé pour extraire des données de diverses sources, les transformer en un format approprié après nettoyage et validation, et les charger dans une destination finale pour l'analyse.

5. **HIVE** : Hive est un système de gestion de données et de requêtes construit sur Hadoop, permettant l'analyse et la manipulation de grandes ensembles de données, utilisant un langage similaire à SQL nommé HiveQL.

6. **Transformation des données** : La transformation des données est le processus de conversion des données brutes en un format ou une structure qui est plus approprié pour l'analyse, la visualisation ou le stockage.

### Contexte

Suite du projet CHU. L'architecture ainsi que la modélisation sont globalement assimilées. La réflexion tourne autour de l'intégration des données.

## Analyser le besoin

### Problème

Certains cas d'intégration de données semblent difficile à réaliser (données manquantes, doublon, formats différents...). On ne sait pas s'il faut transformer les données avant ou après le chargement.

### Contraintes

- Données fournies
- Description des analyses à réaliser
- Le temps : projet avec un timing serré

## Livrables

- Référentiel de données finalisé
- Modélisation multidimensionnelle validée et finalisée
- Intégration des données : jobs nécessaires pour alimenter le schéma décisionnel

## Exemple de plan d'actions

- Etudier le principe des systèmes décisionnels
- Mettre en place le référentiel de stockage de données (Data Lake)
- Valider le schéma décisionnel
- Etudier le principe d'intégration des données et notamment la différence ETL/ELT
- Réaliser l'intégration des données
- Documenter pour livrable 1 du projet