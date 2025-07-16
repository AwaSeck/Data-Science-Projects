# Régression Linéaire Avancée - Analyse du Prix de l'Immobilier

Ce projet vise à prédire le prix de maisons à partir de caractéristiques structurées (surface, nombre de chambres, score des écoles, taux de criminalité...).  
Il permet de mettre en pratique toutes les étapes d’un pipeline de Machine Learning : de la préparation des données à l'interprétation des résultats.

## Objectifs pédagogiques
- Prétraiter un dataset réaliste (valeurs manquantes, outliers, normalisation)
- Comparer des modèles de régression linéaire avancés (Ridge, Lasso, ElasticNet)
- Comprendre les effets de la régularisation et du surajustement
- Évaluer les modèles avec des métriques pertinentes
- Visualiser les performances et interpréter les résultats

---

##  Dataset
> **Dataset simulé inspiré du Boston Housing** (features enrichies)

| Feature | Description |
|--------|-------------|
| `surface` | Surface habitable (m²) |
| `chambres` | Nombre de chambres |
| `salles_bain` | Nombre de salles de bain |
| `age_maison` | Âge de la maison (années) |
| `distance_centre` | Distance au centre-ville (km) |
| `crime_rate` | Taux de criminalité |
| `ecoles_score` | Score des écoles (0-100) |
| `transport_access` | Accessibilité aux transports (1-10) |
| `jardin` | Présence d’un jardin (0/1) |
| `garage` | Nombre de places de garage |
| `prix` | **Prix de vente (€)** (target)

---

## Étapes du projet

### 1. Analyse exploratoire
- Statistiques descriptives, détection des valeurs manquantes
- Traitement des outliers avec la méthode IQR
- Visualisations (corrélations, distributions, scatter plots)

### 2. Feature Engineering
- Création de nouvelles variables (ex : surface_par_chambre, score_quartier)
- Encodage catégoriel, normalisation

### 3. Modélisation
- Régression linéaire de base
- **Ridge, Lasso, Elastic Net** avec cross-validation
- Régression polynomiale (degré 2)

### 4. Évaluation & Comparaison
- MSE, RMSE, MAE, R²
- Résidus vs prédictions
- Importance des variables

### 5. Recommandations
- Interprétation des coefficients
- Impact des variables sur le prix
- Discussion sur le biais/variance et la généralisation

---

##  Résultats obtenus
- **Lasso** a permis de sélectionner automatiquement les variables les plus significatives
- **ElasticNet** a obtenu le meilleur compromis entre biais et variance
- Le modèle final permet de prédire le prix des maisons avec un **R² > 0.88** sur les données test

---

## 📁 Accès aux fichiers
- 📓 Notebook Jupyter : [`Regression_Housing_Price.ipynb`](./Regression_Housing_Price.ipynb)
- 📄 Dataset simulé : [`boston_extended.csv`](./boston_extended.csv)
- 📑 Rapport interprétatif inclus à la fin du notebook

---

## 💡 Compétences développées
- Nettoyage et préparation des données réelles
- Modélisation avec **Scikit-Learn**
- Régularisation et validation croisée
- Visualisation avancée avec Seaborn / Matplotlib
- Interprétation des modèles linéaires

