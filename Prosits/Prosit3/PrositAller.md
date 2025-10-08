# Prosit 3 - Prosit Aller

## Prendre connaissance de la situation et la clarifier

### Mots inconnus

Hive, Hadoop, partitionnement, ETL, calculs d'agrégation, modèle physique, performance, optimisation du traitement, parallélisation des tâches

#### Définitions rapides

1. **Hive** : Hive est un système de gestion de données et de requêtes construit sur Hadoop, permettant l'analyse et la manipulation de grandes ensembles de données, utilisant un langage similaire à SQL nommé HiveQL.

2. **Hadoop** : Hadoop est un framework open source conçu pour le stockage et le traitement distribué de grandes ensembles de données à l'aide de modèles de programmation simples et de composants matériels standard.

3. **Partitionnement** : Le partitionnement dans le contexte du big data fait référence à la division d'un grand ensemble de données en segments plus petits et plus gérables, permettant des traitements plus rapides et plus efficaces.

4. **ETL (Extract, Transform, Load)** : ETL est un processus en trois étapes utilisé pour extraire des données de diverses sources, les transformer en un format approprié après nettoyage et validation, et les charger dans une destination finale pour l'analyse.

5. **Calculs d'agrégation** : Les calculs d'agrégation dans le big data sont des opérations qui réduisent les ensembles de données en calculant des mesures statistiques, comme la somme, la moyenne ou le maximum, souvent utilisées pour obtenir des résumés ou des insights sur les données.

6. **Modèle physique** : Le modèle physique en big data se réfère à la représentation concrète et optimisée de la structure des données dans un système de gestion de base de données, incluant la manière dont les données sont stockées, indexées et accessibles.

7. **Performance** : Dans le big data, la performance se réfère à la rapidité et à l'efficacité avec lesquelles les systèmes de données peuvent traiter et récupérer de grandes quantités de données.

8. **Optimisation du traitement** : L'optimisation du traitement en big data implique l'amélioration de l'efficacité des processus de traitement des données, en réduisant le temps d'exécution et les ressources utilisées, souvent par des ajustements algorithmiques ou des améliorations de configuration.

9. **Parallélisation des tâches** : La parallélisation des tâches dans le big data est la technique de division d'un processus de traitement de données en plusieurs sous-tâches qui peuvent être exécutées simultanément sur différents processeurs ou serveurs, afin d'accélérer le traitement global.


### Contexte

Suite du projet CHU. Vous avez participé à une réunion avec les futurs utilisateurs pour cadrer la mise en place de la solution.

 
## Analyser le besoin

### Problème

- Comment intégrer le processus de mise à jour des données et l'intégration de nouvelles analyses ?
- Comment réaliser les requêtes permettant de sortir les analyses souhaitées ?
- Comment optimiser les traitements pour respecter la contrainte de performance ?

## Contraintes

- Données fournies
- Description des analyses à réaliser
- Nouveau processus induisant une mise à jour des données et de nouvelles analyses tous les 3 mois
- Performance : temps max de traitement pour une analyse : 2min
- Délais : 3 jours pour aboutir aux analyses demandées

## Livrables

- Création et chargement des données dans la base
- Requêtes pour la réalisation des analyses
- Mesures de performance

## Recherche à se poser

- Comment imaginez-vous le passage du modèle conceptuel au modèle physique ?
- Faut-il prévoir des adaptations au modèle physique en fonction des analyses visées ?
- Pourquoi semble-t-il nécessaire de revenir sur l'utilisation de l'ETL dans la mise en place du modèle physique ?
- Voyez-vous des précautions à prendre pour le remplissage des tables ?
- Pourquoi les données ont-elles besoin d'être mises à jour tous les 3 mois ?
- Quel sera l'impact de l'intégration de nouvelles données, de nouvelles analyses ? Faudra-t-il reprendre toute la modélisation ?
- Pensez-vous qu'il existe différents types de SGBD NOSQL ? En quoi pourraient-ils être différents ?
- En quoi peut consister le système de partitionnement de Hive ?
- En quoi consiste map-reduce ? comment imaginez-vous la parallélisation du traitement ?
- Pouvez-vous imaginer d'autres manières d'optimiser les performances du traitement ?

## Exemple de plan d'actions

- Etudier le principe des SGBD NOSQL
- Etudier l'architecture Hive
- Etudier le système de partitionnement de Hive
- Créer la base physique
- Charger les données dans la base
- Créer les requêtes pour la réalisation des analyses
- Mesurer les performances
- Etudier les moyens d'optimisation de traitement et les appliquer
- Etudier l'impact de la mise à jour des données et de la définition de nouvelles analyses tous les 3 mois et adapter la base en conséquence
