# Projet DBT - Transformations Yellow Taxi 2024

## Description
Ce projet utilise **DBT** avec **DuckDB** pour transformer les données Yellow Taxi de New York (année 2024).  
L'objectif est de nettoyer, filtrer et enrichir les données pour analyses et visualisations ultérieures.

### Flux de travail
1. **Sources** : Fichiers `.parquet` bruts (chaque mois) stockés dans `data/`.
2. **Exploration** : Vérification de la qualité des données (passenger_count > 0, total_amount > 0, trip_distance > 0, etc.).
3. **Transformations DBT** :
   - Modèles SQL dans `models/` appliquant les filtres et conversions.
   - Tests DBT dans `tests/` pour valider la cohérence des données.
4. **Output** : Fichier `transformed_data.parquet` généré dans `output/`, prêt à être utilisé par d’autres.

### Utilisation
1. Installer un environnement Python et activer `venv`.
2. Installer DBT et DuckDB :  
   ```bash
   pip install dbt-duckdb duckdb

### Exécuter les transformations DBT :
dbt run

### Vérifier les tests :
dbt test

Le fichier transformé final est disponible dans output/transformed_data.parquet.
