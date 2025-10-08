# Correction

Voici des elements de correction pour l'exercice 1. La correction n'est pas complète mais donne une idée des attentes pour chaque phase de l'exercice.

## Phase 1 : Conception du Schéma en Étoile

### Développement du Schéma

1. **Tables de Faits**

   - **Transactions de Vente**
     - Attributs : TransactionID, DateKey, CustomerKey, ProductKey, CampaignKey, GeoKey, Quantity, TotalSales
   - **Interactions Sociales**
     - Attributs : InteractionID, DateKey, CustomerKey, SentimentKey, Text

2. **Tables de Dimensions**
   - **Temps (DateKey)**
     - Attributs : DateKey, FullDate, Year, Quarter, Month, Week, Day
   - **Client (CustomerKey)**
     - Attributs : CustomerKey, FirstName, LastName, Email, Gender, Age, MembershipLevel
   - **Produit (ProductKey)**
     - Attributs : ProductKey, ProductName, Brand, Category, Price
   - **Campagne (CampaignKey)**
     - Attributs : CampaignKey, CampaignName, StartDate, EndDate, Budget
   - **Sentiment (SentimentKey)**
     - Attributs : SentimentKey, SentimentScore, SentimentLabel
   - **Géographie (GeoKey)**
     - Attributs : GeoKey, Country, Region, City, PostalCode

### Diagramme

Pour représenter un diagramme en étoile en format ASCII pour l'exercice de conception et optimisation d'un Data Warehouse avancé pour l'analyse intégrée des ventes et des interactions en ligne, voici un exemple simple qui montre la structure de la base de données :

```ascii
                               +------------------+
                               |     Temps        |
                               |------------------|
                               | - DateKey (PK)   |
                               | - FullDate       |
                               | - Year           |
                               | - Quarter        |
                               | - Month          |
                               | - Week           |
                               | - Day            |
                               +--------+---------+
                                        |
                                        |
                    +-------------------+--------------------+
                    |                                      |
       +------------v------------+             +------------v------------+
       |   Transactions de Vente  |             |  Interactions Sociales  |
       |--------------------------|             |-------------------------|
       | - TransactionID (PK)     |             | - InteractionID (PK)    |
       | - DateKey (FK)           |             | - DateKey (FK)          |
       | - CustomerKey (FK)       |             | - CustomerKey (FK)      |
       | - ProductKey (FK)        |             | - SentimentKey (FK)     |
       | - CampaignKey (FK)       |             | - Text                  |
       | - SentimentKey (FK)      |             +------------+------------+
       | - GeoKey (FK)            |                          |
       | - Quantity               |                          |
       | - TotalSales             |                          |
       +------------+-------------+                          |
                    |                                        |
                    |                                        |
+------------+------+-------+          +---------------------+------------+
|                        |                                     |
|                        |                                     |
+-----v-----+    +-------v-------+    +---------v---------+    +-------v--------+
|  Client   |    |   Produit    |    |    Campagne       |    |   Sentiment    |
|-----------|    |--------------|    |-------------------|    |----------------|
| - CustomerKey  | - ProductKey  |   |  - CampaignKey    |    | - SentimentKey      |
|   (PK)    |    |   (PK)       |    | - CampaignName    |  | - SentimentScore    |
| - FirstName   | - ProductName |    |   - StartDate     |     | - SentimentLabel    |
| - LastName    | - Brand       |    |  - EndDate        |    |                     |
| - Email       | - Category    |    |   - Budget        |     |                     |
| - Gender      | - Price       |     |                  |     |                |
| - Age         |              |      |                  |     |                |
| - MembershipLevel |              |  |                  |     |                |
+-------------+    +--------------+    +------------------+    +----------------+
```

### Description du Diagramme

- **Tables de Faits** : Ce diagramme montre deux tables de faits principales, **Transactions de Vente** et **Interactions Sociales**, qui stockent les détails des transactions commerciales et des interactions sur les réseaux sociaux respectivement.
- **Tables de Dimensions** : Chaque table de faits est liée à plusieurs tables de dimensions. La dimension **Temps** est commune à toutes les deux, indiquant le moment des transactions et des interactions. Les autres dimensions (**Client**, **Produit**, **Campagne**, et **Sentiment**) sont liées selon la pertinence pour chaque table de faits.
- **Clés Primaires (PK) et Étrangères (FK)** : Les identifiants uniques pour chaque table sont indiqués comme clés primaires (PK), et les liens entre les tables de faits et les tables de dimensions sont marqués comme clés étrangères (FK).

## Phase 2 : Intégration et Transformation des Données avec Talend

### Configuration des Flux de Données

1. **Lecture des Données**
   - Utiliser `tFileInputDelimited` pour lire les données depuis des fichiers CSV pour chaque type de données : transactions, interactions sociales, clients, etc.

### Transformations Nécessaires

1. **Nettoyage des Données**

    - **Standardisation des Dates :** Utiliser `tMap` pour transformer les formats de date incohérents en un format standard (YYYYMMDD). Appliquer une regex pour convertir les formats comme `DD/MM/YYYY` et `YYYY-MM-DD` en `YYYYMMDD`.
    - **Correction des Adresses Email :** Utiliser `tMap` pour corriger ou filtrer les emails incorrects en utilisant des expressions régulières pour valider les formats d'email.

    - Expression Régulière pour les Dates

    ```regex

    (\d{4})[-/](\d{2})[-/](\d{2})

    ```

    - Expression Régulière pour les Emails :

    ```regex

    ^(?![\w+-.]*\.\.)(?!.*@.*@)[\w+-.]+@(?:[a-zA-Z0-9-]+\.)+[a-zA-Z]{2,}$

    ```

    Cette expression vérifie que :

    - Il n'y a pas de points consécutifs dans la partie locale de l'adresse ((?![\w+-.]\*\.\.)).
    - Il n'y a qu'une seule arobase dans l'email ((?!._@._@)).
    - La partie locale de l'adresse peut inclure des lettres, des chiffres, des underscores, des points, des plus et des moins ([\w+-.]+).
    - Le domaine de l'email contient au moins un élément avec un point suivi par deux caractères ou plus dans le top-level domain (TLD), et peut contenir des tirets ((?:[a-zA-Z0-9-]+\.)+[a-zA-Z]{2,}).

2. **Enrichissement des Données**

   - **Jointure avec les Dimensions :** Utiliser `tJoin` pour enrichir les données de la table de faits avec des clés étrangères issues des tables de dimensions après leur nettoyage et standardisation.

3. **Transformation Spécifique pour les Interactions Sociales**

   - **Extraction de Sentiments :** Intégrer une fonctionnalité d'analyse de texte pour extraire des scores de sentiment à partir des textes des interactions. Utiliser `tSentimentAnalysis` si disponible, ou intégrer une API externe via `tRest` pour effectuer cette analyse.

4. **Chargement dans le Data Warehouse**
   - Utiliser `tOutputDelimited` ou directement `tHiveOutput` pour charger les données transformées dans Hive.

## Phase 3 : Optimisation sur Hive

### Optimisation des Requêtes

1. **Partitionnement des Tables**

   - Partitionner les tables de faits selon des clés comme `DateKey` et `GeoKey` pour optimiser les requêtes par période ou par région.

2. **Indexation**

   - Créer des index sur les colonnes fréquemment interrogées telles que `CustomerKey` et `ProductKey` pour améliorer les performances des requêtes.

3. **Optimisation des Formats de Stockage**
   - Utiliser des formats de stockage colonnaires comme ORC pour améliorer la vitesse de lecture et la compression des données.
