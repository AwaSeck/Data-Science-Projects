# Classification d'images : Chats vs Chiens

Ce projet utilise le Deep Learning pour classifier des images de chats et de chiens à partir du dataset de Kaggle. Il est construit de manière progressive, en testant plusieurs approches pour améliorer la performance du modèle.

## Objectif

L'objectif est de construire un modèle capable d'identifier s'il s'agit d'un chat ou d'un chien sur une image. Le projet est également un exercice pratique de renforcement de compétences en Deep Learning.

## Étapes du projet

Le projet est structuré en trois étapes majeures :

1. **Modèle CNN simple**  
   - Création d'un modèle convolutionnel de base avec Keras
   - Entraînement sur un sous-ensemble de données

2. **Transfer Learning**  
   - Utilisation d’un modèle pré-entraîné (VGG16) pour améliorer la performance
   - Congélation des couches convolutives, entraînement des couches supérieures

3. **Data Augmentation et amélioration du modèle**  
   - Ajout de transformations d’images (flip horizontal, zoom, rotation, etc.)
   - Optimisation de la généralisation du modèle
   - Évaluation finale

## Données

- **Source** : [Compétition Kaggle Dogs vs. Cats](https://www.kaggle.com/c/dogs-vs-cats/data)
- **Contenu** : 25 000 images (12 500 chats et 12 500 chiens)
- **Prétraitement** : redimensionnement, séparation en dossiers d'entraînement et validation

> Remarque : les données ne sont pas incluses dans ce dépôt. Il est nécessaire de les télécharger depuis Kaggle.

## Organisation du dépôt

Data-Science-Projects/

│
├── cats-dogs-classification/
│ ├── cats-dogs-classification.ipynb # Notebook principal du projet
│ └── README.md # Fichier explicatif




## Résultats attendus

| Méthode                     | Précision approximative |
|----------------------------|--------------------------|
| CNN simple                 | ~75%                     |
| Avec Transfer Learning     | ~85%                     |
| Avec Data Augmentation     | ~88% - 90%               |

Les résultats varient selon le nombre d’épochs, la taille du jeu d’entraînement, et la puissance de calcul utilisée.

## Environnements compatibles

- Jupyter Notebook / Google Colab
- Python 3.8+
- Bibliothèques : `TensorFlow`, `Keras`, `NumPy`, `Matplotlib`, `Pandas`

## Pour aller plus loin

- Essayer d'autres architectures (ResNet, MobileNet, EfficientNet)
- Intégrer le suivi de l'entraînement avec TensorBoard ou MLflow
- Déployer une interface web avec Flask ou Streamlit
- Réduire la taille du modèle pour une utilisation mobile

## Auteur

**Awa Seck**  
Data Scientist   
Montpellier, France

GitHub : [https://github.com/AwaSeck](https://github.com/AwaSeck)


