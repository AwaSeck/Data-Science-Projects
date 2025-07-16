# Projet 1 : Prédiction Prix Immobilier 🏠
## Régression Linéaire Avancée

### 📋 Objectifs pédagogiques
- Maîtriser le preprocessing des données réelles
- Comparer différents modèles de régression
- Comprendre la régularisation (Ridge, Lasso, Elastic Net)
- Évaluer et interpréter les performances
- Visualiser les résultats de manière professionnelle

### 🎯 Livrables attendus
1. **Notebook Jupyter** complet avec analyse
2. **Rapport d'analyse** (2-3 pages)
3. **Modèle sauvegardé** prêt pour la production
4. **Script Python** pour prédictions futures

---

## 📊 Dataset
**Boston Housing Dataset étendu** (nous utiliserons un dataset simulé plus riche)

**Variables disponibles :**
- `surface` : Surface habitable (m²)
- `chambres` : Nombre de chambres
- `salles_bain` : Nombre de salles de bain
- `age_maison` : Âge de la maison (années)
- `distance_centre` : Distance du centre-ville (km)
- `crime_rate` : Taux de criminalité du quartier
- `ecoles_score` : Score moyen des écoles (0-100)
- `transport_access` : Accessibilité transports (1-10)
- `jardin` : Présence d'un jardin (0/1)
- `garage` : Nombre de places de garage
- `prix` : **Prix de vente (€)** [VARIABLE CIBLE]

---

## 🔧 Étapes du projet

### Phase 1 : Exploration et Preprocessing (Jour 1)
```python
# Template de démarrage
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.linear_model import LinearRegression, Ridge, Lasso, ElasticNet
from sklearn.metrics import mean_squared_error, r2_score, mean_absolute_error
import warnings
warnings.filterwarnings('ignore')

# TODO: Chargement et exploration des données
# 1. Chargez le dataset (je vous fournirai le code)
# 2. Analysez les statistiques descriptives
# 3. Identifiez les valeurs manquantes
# 4. Détectez les outliers
# 5. Créez des visualisations exploratoires
```

**Questions d'analyse :**
- Quelles variables sont les plus corrélées au prix ?
- Y a-t-il des outliers à traiter ?
- Les données suivent-elles une distribution normale ?

### Phase 2 : Feature Engineering (Jour 1-2)
```python
# TODO: Création de nouvelles variables
# 1. surface_par_chambre = surface / chambres
# 2. ratio_sdb_chambres = salles_bain / chambres
# 3. score_quartier = (ecoles_score + transport_access) / 2
# 4. Variables catégorielles pour âge_maison (neuf, récent, ancien)
# 5. Interaction features si pertinentes
```

### Phase 3 : Modélisation (Jour 2-3)
**Modèles à implémenter :**
1. **Régression Linéaire Simple**
2. **Ridge Regression** (avec cross-validation pour alpha)
3. **Lasso Regression** (avec cross-validation pour alpha)
4. **Elastic Net** (avec optimisation des hyperparamètres)
5. **Régression Polynomiale** (degré 2)

```python
# TODO: Implémentation des modèles
# 1. Division train/validation/test (60/20/20)
# 2. Normalisation des features
# 3. Entraînement de chaque modèle
# 4. Validation croisée (5-fold)
# 5. Optimisation des hyperparamètres
```

### Phase 4 : Évaluation et Comparaison (Jour 3)
**Métriques à calculer :**
- MSE (Mean Squared Error)
- RMSE (Root Mean Squared Error)
- MAE (Mean Absolute Error)
- R² Score
- MAPE (Mean Absolute Percentage Error)

```python
# TODO: Tableau de comparaison des modèles
# Créer un DataFrame avec toutes les métriques
# Visualisation des résidus
# Feature importance pour Lasso
```

### Phase 5 : Visualisations (Jour 3-4)
**Graphiques attendus :**
1. Matrice de corrélation
2. Distribution des variables
3. Scatter plots prix vs features importantes
4. Résidus vs prédictions
5. Comparaison visuelle des modèles
6. Feature importance

### Phase 6 : Interprétation et Rapport (Jour 4)
**Rapport structuré :**
1. **Executive Summary**
2. **Analyse exploratoire**
3. **Méthodologie**
4. **Résultats et comparaisons**
5. **Recommandations business**
6. **Limites et améliorations**

---

## 📝 Critères d'évaluation (sur 20 points)

### Code et Technique (12 points)
- **Preprocessing** (3 pts) : Gestion valeurs manquantes, outliers, normalisation
- **Feature Engineering** (2 pts) : Créativité et pertinence des nouvelles variables
- **Modélisation** (4 pts) : Implémentation correcte, hyperparamètres optimisés
- **Évaluation** (3 pts) : Métriques appropriées, validation croisée

### Analyse et Interprétation (5 points)
- **Visualisations** (2 pts) : Clarté, pertinence, esthétique
- **Insights** (2 pts) : Compréhension des résultats, recommandations
- **Rapport** (1 pt) : Structure, clarté, professionnalisme

### Bonnes Pratiques (3 points)
- **Code propre** (1 pt) : Commentaires, structure, lisibilité
- **Reproductibilité** (1 pt) : Random seeds, requirements.txt
- **Documentation** (1 pt) : Docstrings, README

---

## 🚀 Pour commencer

1. **Créez le dossier** : `~/ML_Projects/01_regression/`
2. **Téléchargez le starter code** que je vais vous fournir
3. **Commencez par l'exploration** des données
4. **Envoyez-moi votre travail** après chaque phase pour feedback

**Temps estimé :** 4-5 jours (avec vos 5h/jour)

**Questions avant de commencer :**
- Avez-vous des préférences pour le style de visualisation ?
- Voulez-vous que je génère le dataset ou préférez-vous un dataset réel ?
- À quelle fréquence voulez-vous mes retours (quotidiens ?) ?

Prêt(e) à commencer ? Je vais créer le code de démarrage avec le dataset !