# Prosit 1 - Prosit Retour

## Définitions

### Big Data (Données massives)

Le Big Data est un type de base de données ayant des caractéristiques spécifiques. Trois règles ont été utilisées pour définir le Big Data. Il s’agit des règles « 3V », « 4V » et « 5V » :

#### Règle des 3V

En 2012, Gartner définit les enjeux inhérents à la croissance des données comme étant tridimensionnels. Il s’agit du Volume, de la Variété et de la Vélocité d’où cette définition : « Les Big Data sont des données volumineuses, très variées, générées et traitées à grande vitesse. Ces données exigent des formes efficaces et innovantes de traitement de l'information pour permettre une meilleure prise de décision ».
  
#### Règle des 4V

Quatre dimensions pour caractériser le Big Data, à savoir : le Volume, la Variété, la Vélocité et la Valeur. Définition : « Les Technologies Big Data décrivent une nouvelle génération de technologies et d’architectures conçues pour extraire économiquement de la valeur à partir de grands volumes de données très variées, en permettant leur capture et leur analyse à grande vitesse ».

#### Règle des 5V

Deux nouveaux V sont apparus en 2013 avec une définition plus large pour le Big Data au travers de la règle des 5V : « Les Technologies Big Data visent à traiter des données de grand volume, grande vélocité et grande variété pour extraire de la valeur, assurer une forte véracité des données originales et obtenir des informations qui exigent des formes novatrices de traitement des données, afin d’améliorer la prise de décision et le contrôle des processus »

Les définitions associées aux dimensions utilisées dans les règles ci-dessus sont les suivantes :

* **Volume** : représente la taille de l'ensemble des données à traiter,
* **Variété** : fait référence à la diversité des sources, des types et des formats de données,
* **Vélocité** : correspond à la vitesse à laquelle les données sont collectées et traitées,
* **Valeur** : équivaut au profit que l'on peut tirer de l'usage des Big Data,
* **Véracité** : recouvre la qualité et la fiabilité des données ; c'est la dimension qualitative des Big Data.

### BI (Business intelligence ou l'informatique décisionnelle)

L’informatique décisionnelle, également Business Intelligence ou BI en anglais, désigne les moyens, les méthodes et les outils qui apportent des solutions en vue d’offrir une aide à la décision aux professionnels afin de leurs permettre d’avoir une vue d’ensemble sur l’activité de l’entreprise et de leurs permettre de prendre des décisions plus avisées à travers des tableaux de bord de suivi et des analyses.

### Modélisation des données

La modélisation des données (data modeling en anglais) est un processus de description de la structure, des associations, des relations et des contraintes relatives aux données disponibles. Elle sert à établir des normes et à coder des règles de gestion (modèles) des données dans l’organisation. Le data modeling fait partie intégrante de la phase de planification de tout déploiement analytique dans l’organisation ou de projet de Business Intelligence. Qu’est-ce qu’un modèle de données ? Dans le processus de modélisation, l’accent est mis sur le besoin de disponibilité et d’organisations des données et non sur la manière dont celles-ci seront utilisées.

### Modélisation dimensionnelle

La conception du modèle conceptuel de données commence par la définition et l’analyse des besoins qui détermine quelles sont les données requises pour répondre aux besoins d'analyse des utilisateurs. Le résultat de cette analyse est le modèle dimensionnel. Ce modèle identifie la granularité de la table de faits, associées aux dimensions avec leurs attributs et leurs hiérarchisations.

### Stockage de données dans le cloud

Le stockage dépend généralement de la technologie de virtualisation utilisée, et surtout de sa « profondeur ». Dans les technologies d'isolation, la virtualisation se fait au niveau de l'OS, et ne nécessite pas un dispositif de stockage particulier : chaque environnement virtualisé se présente sous la forme d'une arborescence gérable depuis le domaine de contrôle. Cette arborescence peut de façon transparente, être située physiquement sur la même machine, sur un autre disque, sur un serveur distant, sur un réseau de stockage, etc. C'est la solution qui offre la plus grande souplesse. Dans les technologies de machine virtuelle, l'hyperviseur ne fournit au système virtualisé qu'un espace de stockage. Il peut s'agir d'un volume, ou simplement d'un fichier, mais dans les deux cas cet espace est «hermétique» et ne peut être accédé depuis le domaine de contrôle. Là encore, on peut placer l'intégralité de cet espace sur un disque local, un réseau de stockage, un autre serveur...

### Stockage en réseau

Dans ce type de stockage, les hyperviseurs sont généralement gérés sous forme de « pools », formant une « force de travail » globale qui se partageront les machines virtuelles à exécuter. Disposant d'un réseau de stockage, chaque hyperviseur a accès à toutes les machines virtuelles, et peut donc exécuter n'importe laquelle, et la transférer sans interruption à un autre hyperviseur en fonction de sa charge.

### Stockage en cluster

Dans ce type de stockage, les hyperviseurs sont gérés sous forme de « clusters », formant une « force de travail » globale qui se partageront les machines virtuelles à exécuter. Disposant d'un réseau de stockage, chaque hyperviseur a accès à toutes les machines virtuelles, et peut donc exécuter n'importe laquelle, et la transférer sans interruption à un autre hyperviseur en fonction de sa charge.

### NAS

Un NAS ou stockage réseau (Network-Attached Storage), est simplement un serveur fournissant leurs fichiers à d'autres serveurs par le réseau.

### NFS

NFS est le standard universel pour l'accès aux fichiers sur un réseau, c'est le protocole le plus utilisé dans les NAS.

### SAN

Un SAN, ou réseau de stockage (Storage Area Network), est un réseau sur lequel circulent les données entre un système et son stockage. Cette technique permet de déporter tout le stockage interne d'une machine vers un équipement dédié.

### Système de fichiers distribué

C'est un système où le poste client accède à un espace de stockage virtuel unique. Les données peuvent être réparties/dupliquées sur plusieurs machines de façon transparente pour celui-ci. C'est le moteur du système de fichiers distribué qui a la charge de répartir les données et de les dispatcher au client. Les systèmes de fichier distribués les plus répandus sont :

* Ceph
* GlusterFS
* Hadoop Distributed File System (HDFS)
* Lustre (utilisé par les super-calculateurs)
* NFS - Network File System

### Hadoop

Hadoop est un système logiciel distribué capable de stocker et traiter de manière séquentielle, et à des coûts raisonnables, des volumes de données de plusieurs péta-octets. Il offre une grande flexibilité (possibilité d’enlever et d’ajouter des machines) et ses performances évoluent de manière quasi linéaire en fonction du nombre de machines constituant le cluster. Hadoop a été écrit en Java, qui demeure le langage de prédilection pour les développeurs de programme Hadoop.

### HDFS

Il s’agit d’un système de gestion de fichiers distribué, inspiré par GFS le système de gestion de fichiers de Google. HDFS est le composant d’Hadoop en charge du stockage de données dans le cluster. Les composantes de HDFS : HDFS se compose d’un ensemble de nœuds :

* **NameNode** : est un nœud maître qui s’occupe de gérer l’état de HDFS. Le NameNode est responsable de la répartition des données sur les DataNode et de la gestion de l’espace mémoire du cluster. Il héberge les métadonnées qui représentent l’ensemble d’information sur l’emplacement des blocs de données, leurs propriétés et les autorisations.
* **SecondaryNameNode** : est aussi un nœud maître. Le SecondaryNameNode est chargé de la maintenance des nœuds du cluster, où il garde sous contrôle l’espace disque utilisé, limite la charge processeur du NameNode et permet la continuité de fonctionnement du cluster Hadoop en cas de panne.
* **DataNode** : est le nœud esclave implanté sur chaque machine du cluster qui n’est pas un nœud maître. Le DataNode héberge une partie des données du cluster Hadoop afin d’assurer une haute disponibilité des données.

### MapReduce

MapReduce est un modèle de programmation conçu pour la lecture et le traitement d’un volume de données très important. Il implémente au sein d’Hadoop diverses fonctionnalités : la division des tâches en parallèle, leurs répartitions et la collecte des résultats. Un programme MapReduce se constitue de fonction map et reduce. La fonction map fait la lecture des données stockées sur disque et les traite. La fonction reduce consolide les résultats issus de la fonction map puis les écrit sur le disque. Les données MapReduce sont lues ou écrites selon le format <clé, valeur>. L’exécution d’un programme MapReduce sur un ensemble de données désigne le job Hadoop. Les composantes de MapReduce : Une tâche, au sens Hadoop du terme, est une tâche map ou une tâche reduce. Chaque tâche traite une partie seulement de l’ensemble des données du cluster. L’exécution de ces tâches est contrôlée par un ensemble de nœuds maîtres et esclaves qui sont :

* **JobTracker** : est le nœud maître responsable du lancement des tâches d’un job Hadoop et de leurs coordinations au niveau des nœuds esclaves. Il est aussi chargé de planifier l’exécution des jobs Hadoop, l’agrégation de leurs résultats et de la gestion de l’état du TaskTracker.
* **TaskTracker** : est le nœud esclave en charge de l’exécution des tâches map et reduce qui lui sont assignées par le JobTracker. Des rapports journaliers regroupant l’ensemble d’informations sur l’exécution des tâches MapReduce sont tenus par le JobTracker, ce qui garantit une facilité de réinitialisation des tâches en cas de défaillance d’un nœud TaskTracker. L’ensemble des nœuds maîtres et esclaves des deux composantes HDFS et MapReduce constituent les composantes du cluster Hadoop.

### Les outils de l’écosystème d’Hadoop

L’écosystème de Hadoop comprend de nombreux outils en supplément de HDFS et MapReduce, tels que représentés dans la figure ci-dessous. Les outils d’Hadoop peuvent être classés en trois grandes catégories :

* Les outils orientés bases de données (Hbase, Scoop,...)
* Les outils de Requêtage et scripting des données Hadoop (Hive, Pig, API Streaming)
* Les outils d’exploitation (Zookeeper, Oozie)

#### Hive

Hive est un projet open source dédié à la construction d’entrepôt de données sous la plateforme Hadoop. Hive utilise un langage de requête semblable à SQL appelé HiveQL, qui prend en charge certaines primitives de manipulation de données telles que la projection, jointure, le groupement, l’union et les sous-requêtes dans la clause FROM. Le plan d’exécution d’une requête HiveQL se traduit par la création et l’exécution d’un ensemble de tâches map et de tâches reduce.

#### Cloudera

Cloudera est une entreprise Américaine basée en Californie, elle se consacre au développement d’une solution Big Data basée historiquement sur le framework distribué Hadoop et qui est en train de se réorienter vers le Cloud. Cloudera développe depuis plus d’un an sa solution dans les Cloud publiques AWS, Azure et GCP.

#### Spark

Apache Spark est un framework open source de calcul distribué conçu pour être rapide et général. Il fournit des API de haut niveau en Java, Scala, Python et R, et un moteur optimisé qui prend en charge la génération de graphiques de traitement de données en parallèle. Il prend en charge une grande variété de charges de travail, notamment le traitement de flux, le traitement par lots, l'apprentissage automatique et l'analyse interactive.

### ETL

Afin d’alimenter le datawarehouse à partir des différentes applications de l’entreprise, on utilise une gamme d’outils appelés ETL, pour « Extract, Transform, Load ». Comme le nom l’indique, ces outils permettent d’extraire des données à partir de différentes sources, de les transformer (format, dénomination), et de les charger dans la base de données cible, ici le datawarehouse.

### Power BI

Power BI est un ensemble de services logiciels, d’applications et de connecteurs qui œuvrent ensemble pour transformer des sources de données disparates en informations visuelles immersives et interactives. Vos données peuvent être sous forme de feuille de calcul Excel ou de collection d’entrepôts de données hybrides locaux ou sur le cloud. Power BI vous permet de vous connecter facilement à vos sources de données, de visualiser et de découvrir ce qui est important, et de partager ces informations avec qui vous voulez.

### Entrepôt de données

C’est un ensemble de magasin de données représentant une collection de données intégrées, variant selon le temps et non volatiles, qui sert de support au processus de prise de décision. La notion d’entrepôts de données a été introduite pour la première fois par Bill. Les données de cette base de données sont intégrées, contenant des informations historisées, non volatiles et destinées à la prise de décision.

### Cycle de vie dimensionnel d’un Entrepôt de données

Les experts dans le domaine adhèrent à la règle que les méthodologies de développement des systèmes décisionnels sont différentes de celles utilisées pour les autres systèmes (transactionnels par exemple). Par ailleurs, un plan de projet global tel que le Cycle de Vie Dimensionnel (CVD) qui permet de mettre en place une solution décisionnelle complète de l'extraction à l'exploitation de l'information.

### Entrepôt de Données de Santé 

Il intègre les données administratives et médicales des millions de patients hospitalisés ou venus en consultation dans les établissements de France.

### Mesures, Faits, Dimensions et Modèles

Les termes "mesures", "faits" et "dimensions" sont des concepts fondamentaux utilisés pour organiser et analyser les données. Ils permettent de créer des rapports, des tableaux de bord, des analyses et des visualisations pour prendre des décisions informées dans le domaine de l'informatique décisionnelle. Ces concepts sont au cœur de la modélisation des données dans les entrepôts de données et des systèmes de business intelligence :

* **Mesures** (ou indicateurs) : Les mesures sont des données quantitatives qui représentent les informations que vous souhaitez analyser. Ce sont les données numériques ou les valeurs sur lesquelles vous souhaitez effectuer des calculs, des agrégations ou des analyses. Par exemple, dans une entreprise, les ventes mensuelles, les revenus, les coûts, la marge bénéficiaire, etc., sont des exemples de mesures.
* **Faits** : Les faits sont des enregistrements ou des lignes de données qui contiennent les mesures associées à un événement ou une transaction spécifique. Les faits sont souvent stockés dans des tables de faits et sont liés à des dimensions pour donner du contexte aux mesures. Par exemple, dans un magasin de données pour la vente au détail, un fait pourrait être une transaction de vente spécifique, et les mesures associées pourraient inclure le montant de la vente, le produit vendu, la date de la transaction, etc.
* **Dimensions** : Les dimensions sont des attributs ou des caractéristiques qui fournissent un contexte aux mesures. Elles permettent de segmenter, de filtrer et d'analyser les mesures. Les dimensions sont souvent organisées en hiérarchies. Par exemple, dans une analyse de ventes, les dimensions pourraient inclure le temps (année, trimestre, mois, jour), le produit (catégorie, marque, modèle), la géographie (pays, région, ville), etc.
* **Modèles dimensionnels** : Les entrepôts de données (data warehouses) utilisent différents modèles pour organiser et stocker les données de manière à faciliter l'analyse et la prise de décision. Voici quelques-uns des modèles couramment utilisés :
  * Modèle en étoile (Star Schema) : Ce modèle est l'un des plus populaires pour les entrepôts de données. Il se caractérise par une table centrale de faits (fact table) contenant les mesures ou les faits, entourée de tables de dimensions (dimension tables) qui décrivent les éléments contextuels des données.
  * Modèle en flocon (Snowflake Schema) : Le modèle en flocon est une variation du modèle en étoile dans lequel les tables de dimensions sont normalisées en sous-dimensions, créant une structure hiérarchique. Cela peut aider à économiser de l'espace de stockage, mais cela peut rendre les requêtes plus complexes
  * Modèle en constellation (Constellation Schema) : Ce modèle consiste en plusieurs schémas en étoile interconnectés, chacun représentant un domaine de données spécifique. Il est utilisé lorsque vous avez des domaines de données distincts qui partagent certaines informations.

### Architecture Big Data

  Les systèmes de bases de données traditionnels ne permettent plus de répondre aux exigences imposées par le Big Data. Ils ne sont pas en mesure de traiter des volumes de données aussi massifs et assez rapidement. C’est pourquoi, pour pouvoir profiter des avantages du Big Data, il faut repousser les limites des systèmes notamment en termes de volume, de vitesse de traitement et de variété des données à manager. Pour cela, il faut adapter la structure son écosystème informatique traditionnel et mettre en place une architecture Big Data. En mettant en place une architecture Big Data adaptée dans son entreprise, une organisation va pourvoir effectuer :

- Un traitement en batch des sources de Big Data
- Un traitement en temps réel des Big Data en mouvement
- Une exploration des données volumineuses
- Une centralisation des data issues de différentes sources et existantes sous différents formats
- Des analyses prédictives
- Des tâches basées sur les technologies du Big Data et de l’intelligence artificielle

#### Les composantes d’une architecture Big Data

La plupart des architectures de données volumineuses incluent tout ou partie des éléments suivants :

- Source de données (data mart, data warehouse, cloud, base de données hybride)
- Stockage (magasin de données, data lake)
- Batch processing (traitement par lots)
- Stream processing (traitement de flux de données)
- Préparation de données
- Data catalog
- Modélisation de données
- Technologie d’orchestration

#### Principaux types d’architecture Big Data

Dans le domaine des Big Data, il existe des problématiques auxquelles aucune technologie, utilisée seule, ne peut apporter de réponse globale. Ainsi, le choix d’une technologie et l’usage qui en sera fait sera en général soumis à deux questions préalables : l’outil est-il évolutif ? Existe-il une courbe d’apprentissage liée à l’expérience de cette technologie, qui permette une réduction des temps de production, dans le temps ? Des architectures big data, comme l’architecture Lambda par exemple, ont donc été conçues pour résoudre des problématiques parfois complexes nécessitant l’intervention de plusieurs technologies. Ces architectures pourraient être comparées aux design patterns dans les langages objets. Les design patterns permettent de répondre à des enjeux liés à la conception d’un programme pouvant garantir la réutilisation et la pérennité du code. Ci-dessous sont listés les types d’architecture qui répondent aux besoins de traitement, de sauvegarde et/ou d’analyse de données :

- Architecture Datalake
- Architecture Lambda
- Architecture Kappa

Il s’agit d’une architecture distribuée qui gère de grosse quantité de données. Cela nous ramène à la problématique de stockage qui dépasse les capacités de traitement et de stockage des systèmes traditionnels qui n’utilisent qu’une machine unique, pour cela, il est nécessaire de mettre en place des architectures dites distribuées. Concrètement, cela revient à diviser la charge de stockage et de traitement d’une machine sur plusieurs machines afin de gagner en rapidité, en réactivité et en performance. Ainsi les solutions Datalake, Lambda et Kappa reposent sur ce système puisque, comme précisé ci-dessous, les tâches d’intégration, de traitement et de stockage sont réparties en plusieurs couches.

- **L’architecture Datalake** :
  Le Datalake (ou lac de données) est une architecture apparue avec les technologies Big Data, permettant le stockage de gros volumes de données. Le Datalake offre aux entreprises un système de stockage permettant d’accueillir tous types de données (brutes ou non) qu’elles soient structurées, semi-structurées et/ou non structurées. Cette architecture big data permet ainsi une transformation et un raffinement rapide des données stockées, que le volume traité soit important ou non. Celle-ci pourrait être définie en un mot : adaptable. Bien que n’étant pas le seul, Hadoop reste le framework de référence le plus utilisé pour la construction d’un Datalake. Les données peuvent provenir de multiples sources comme des logs, des services web, etc. Les différents systèmes d’ingestion consommeront les données pour ensuite les insérer dans le Datalake (HDFS). Une fois que les données sont enregistrées, les systèmes d’interrogations pourront alors interroger le Datalake.

- **L’architecture Lambda** :
  Créée par Nathan Marz, c’est l’architecture la plus couramment utilisée pour le traitement et la gestion des données volumineuses en temps réel et par lots de manière simultanée. L’architecture Lambda se découpe en 3 couches :

- Couche batch (Batch Layer) :
  - Stockage de l’ensemble des données
  - Traitements massifs et réguliers
  - La fréquence des traitements ne doit pas être trop importante afin de minimiser les tâches de fusion des résultats pour constituer les vues
- Couche temps réel (Speed Layer) :
  - Traite tout type de donnée reçu en temps réel
  - Calcule des vues incrémentales qui vont compléter les vues batch afin de fournir des données plus récentes
  - Suppression des vues temps réel obsolètes (postérieures à un traitement batch)
- Couche de service (Serving Layer) :
  - Permet de stocker et d’exposer aux clients les vues créées par les couches batch et temps réel
  - Adapté à tous types de bases NoSQL
      L’architecture Lambda sera souvent utilisée pour obtenir une vision complète des données.

- **L’architecture Kappa**

  L’architecture KAPPA a été pensée pour pallier la complexité de l’architecture Lambda. Elle repose sur le principe de fusion de la couche temps réel et batch, ce qui la rend moins complexe que l’architecture Lambda. Ne permettant pas le stockage de manière permanente, cette architecture est faite pour le traitement de données. Kappa n’étant également pas liée à une seule technologie, vous pouvez y associer différents outils, comme le montre le schéma ci-dessous :

- Stockage/temps réel : Kafka permet la sauvegarde des messages pour pouvoir ensuite les retraiter
- Traitements : Storm, Spark
- Couche de service : Cassandra, Hive, HBase, Outil maison, etc…

