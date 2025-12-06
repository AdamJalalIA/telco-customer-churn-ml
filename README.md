![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0+-green.svg)
![XGBoost](https://img.shields.io/badge/XGBoost-1.5+-green.svg)

# Customer Churn Prediction

Projet de machine learning pour prédire le churn des clients d'une entreprise de télécommunications.

## Description

Ce projet utilise le dataset Telco Customer Churn de Kaggle pour construire des modèles de classification capables de prédire si un client va quitter l'entreprise. J'ai testé plusieurs modèles (Logistic Regression, Random Forest, XGBoost) et comparé leurs performances.

## Dataset

Le dataset contient environ 7000 clients avec 21 features incluant des informations démographiques, les services souscrits, le type de contrat, et les charges mensuelles. Le taux de churn est d'environ 27%.

Le dataset est disponible sur Kaggle : https://www.kaggle.com/datasets/blastchar/telco-customer-churn

Il faut télécharger le fichier WA_Fn-UseC_-Telco-Customer-Churn.csv et le placer dans le répertoire du projet.

## Installation

Les dépendances principales sont :
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
- xgboost
- imbalanced-learn

Pour installer :
```
pip install pandas numpy matplotlib seaborn scikit-learn xgboost imbalanced-learn
```

## Utilisation

Ouvrir le notebook churn_prediction.ipynb avec Jupyter et exécuter les cellules dans l'ordre.

## Approche

Le projet suit un pipeline classique de machine learning :

1. Exploration des données et nettoyage
2. Encodage des variables catégorielles
3. Feature engineering pour créer de nouvelles variables
4. Analyse de corrélation
5. Préparation des features et de la variable cible
6. Division train/test
7. Gestion du déséquilibre de classes avec SMOTE
8. Entraînement de trois modèles (XGBoost avec optimisation d'hyperparamètres)
9. Validation croisée
10. Évaluation avec métriques diverses
11. Analyse de l'importance des features

## Modèles testés

- Logistic Regression : modèle linéaire avec standardisation des features
- Random Forest : modèle d'ensemble avec 100 estimateurs
- XGBoost : gradient boosting optimisé avec RandomizedSearchCV

## Métriques

Les modèles sont évalués avec plusieurs métriques :
- Accuracy
- Precision
- Recall
- F1-Score (métrique principale)
- AUC-ROC
- Matrices de confusion
- Courbes ROC et Precision-Recall

## Résultats

Les trois modèles donnent des performances similaires avec un F1-Score autour de 0.80-0.85. Random Forest et XGBoost sont légèrement meilleurs que Logistic Regression. Les features les plus importantes pour prédire le churn sont généralement tenure, MonthlyCharges, TotalCharges, et le type de contrat.

## Structure

```
telco-customer-churn-ml/
├── churn_prediction.ipynb
├── README.md
└── WA_Fn-UseC_-Telco-Customer-Churn.csv
```

## Auteur

Adam Jalal
