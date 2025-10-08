# Correction

Voici des elements de correction pour l'exercice 1. La correction n'est pas complète mais donne une idée des attentes pour chaque phase de l'exercice.

## Phase 1 : Modélisation en Étoile

**1. Identification des éléments clés pour la table de faits et pour chaque dimension:**

- **Table de Faits (Transactions de Ventes)**
  - Attributs: TransactionID, DateKey, CustomerKey, ProductKey, GeoKey, Quantity, TotalSales.
- **Dimensions:**
  - **Temps (DateKey)**
    - Attributs: DateKey, Date, Day, Month, Year, DayOfWeek, WeekOfYear, Quarter.
  - **Client (CustomerKey)**
    - Attributs: CustomerKey, FirstName, LastName, Email, Gender, Age, MembershipLevel, RegistrationDate.
  - **Produit (ProductKey)**
    - Attributs: ProductKey, ProductName, Brand, Category, Price, Supplier.
  - **Géographie (GeoKey)**
    - Attributs: GeoKey, Country, Region, City, PostalCode.

**2. Création d'un diagramme de schéma en étoile:**
Imaginez un diagramme central où la table de faits est au milieu, entourée par les dimensions Temps, Client, Produit, et Géographie, chacune liée par une clé étrangère à la table de faits.

### Phase 2 : Intégration avec Talend

**Description des flux de données dans Talend pour peupler le schéma en étoile:**

- **Extraction des Données:**
  - Utilisation des composants tFileInputDelimited pour charger les données depuis les fichiers CSV.
- **Transformations de Données:**
  - Utilisation de tMap pour les transformations nécessaires, comme le nettoyage des formats de date incohérents (par exemple, convertir "2023/01/01" en "20230101").
  - Utilisation de tFilterRow pour filtrer les enregistrements indésirables ou incomplets.
  - Utilisation de tJoin pour enrichir les données de la table de faits avec des clés étrangères issues des tables de dimensions après leur nettoyage.
- **Chargement dans le Data Warehouse:**
  - Utilisation de tOutputDelimited pour charger les données nettoyées et transformées dans des fichiers de données prêts pour Hive.

### Phase 3 : Optimisation sur Hive

**Proposition de méthodes pour optimiser les requêtes sur le Data Warehouse:**

- **Partitionnement des Tables:**
  - Partitionner la table de faits par `DateKey` et potentiellement par `GeoKey` pour améliorer les performances des requêtes filtrées par date ou géographie.
- **Bucketing:**
  - Utiliser le bucketing sur la table de produits par `ProductKey` pour une distribution équilibrée des données et une amélioration des jointures.
- **Indexation:**
  - Créer des index sur les colonnes fréquemment utilisées dans les requêtes, comme `CustomerKey` dans la table de clients, pour accélérer les recherches.

**Exemple de script Hive pour créer une table partitionnée:**

```sql
CREATE TABLE transactions (
    TransactionID int,
    CustomerKey int,
    ProductKey int,
    Quantity int,
    TotalSales double
)
PARTITIONED BY (DateKey int, GeoKey int)
STORED AS ORC tblproperties ("orc.compress" = "SNAPPY");
```
