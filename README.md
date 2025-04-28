# Baseball AI

## Description
Ce projet vise à développer un modèle prédictif pour les résultats des matchs de baseball de la MLB. L'objectif est de créer un système qui analyse les données historiques et actuelles des équipes et des joueurs pour prédire les résultats des matchs à venir avec la plus grande précision possible.

## Table des matières
- [Objectifs](#objectifs)
- [Structure du projet](#structure-actuelle-du-projet)
- [Données](#données)
- [Méthodologie](#méthodologie)
- [Modèles](#modèles)
- [Interface utilisateur](#interface-utilisateur)
- [Évaluation des performances](#évaluation-des-performances)
- [Améliorations futures](#améliorations-futures)

## Objectifs
- Collecter et préparer les données historiques des matchs de MLB
- Analyser les facteurs influençant les résultats des matchs
- Développer un modèle prédictif robuste 
- Évaluer la performance du modèle
- Créer une interface utilisateur intuitive avec Streamlit
- Permettre aux utilisateurs de visualiser les prédictions pour les matchs à venir

## Structure actuelle du projet
```
├── baseball_ai
│   ├── Data
│   │   ├── catboost_info
│   │   │   ├── catboost_training.json
│   │   │   ├── learn
│   │   │   │   └── events.out.tfevents
│   │   │   ├── learn_error.tsv
│   │   │   ├── time_left.tsv
│   │   │   └── tmp
│   │   ├── clean
│   │   │   ├── mlb_games_2017_2024.csv
│   │   │   ├── mlb_pitchers_stats_2017_2024.csv
│   │   │   └── mlb_teams_stats_2017_2024.csv
│   │   ├── exploration_data.ipynb
│   │   ├── exploration_model.ipynb
│   │   └── raw
│   │       ├── mlb_games_2017_2023.csv
│   │       ├── mlb_games_2024.csv
│   │       ├── mlb_pitchers_2017_2024.csv
│   │       ├── mlb_pitchers_stats_2017_2022.csv
│   │       └── mlb_pitchers_stats_2023_2024.csv
│   └── __init__.py
├── catboost_info
│   ├── catboost_training.json
│   ├── learn
│   │   └── events.out.tfevents
│   ├── learn_error.tsv
│   ├── time_left.tsv
│   └── tmp
├── Makefile
├── README.md
└── requirements.txt
```

## Données
Les données utilisées dans ce projet comprennent :
- Historique des matchs de MLB (résultats, scores)
- Statistiques des équipes (attaque, défense, lanceurs)
- Statistiques individuelles des joueurs
- Données contextuelles (météo, stade, etc.)

Sources de données :
- API officielle de la MLB
- Baseball-Reference
- Statcast

## Méthodologie
1. **Collecte de données** : Extraction des données historiques et actuelles via API et web scraping
2. **Prétraitement** : Nettoyage et intégration des données provenant de différentes sources
3. **Analyse exploratoire** : Identification des tendances et des corrélations
4. **Ingénierie des caractéristiques** : Création de caractéristiques pertinentes pour le modèle
5. **Sélection du modèle** : Test de différents algorithmes de machine learning
6. **Entraînement et validation** : Utilisation de validation croisée pour optimiser les hyperparamètres
7. **Évaluation** : Mesure de la performance sur un ensemble de test indépendant
8. **Déploiement** : Intégration du modèle dans une interface Streamlit

## Modèles
Nous prévoyons de tester plusieurs types de modèles :
- Régression logistique
- Forêts aléatoires
- Gradient Boosting (XGBoost, LightGBM)
- DNN / RNN
- Modèles d'ensemble

## Interface utilisateur
L'interface utilisateur sera développée avec Streamlit et offrira les fonctionnalités suivantes :
- Visualisation des prédictions pour les matchs à venir
- Affichage des facteurs clés influençant chaque prédiction
- Historique des performances du modèle
- Comparaison des statistiques des équipes
- (Tableau de bord interactif pour explorer les données)

## Évaluation des performances
Le modèle sera évalué sur une métrique principale :
- Précision

## Améliorations futures
- Intégration de données en temps réel
- Ajout de facteurs supplémentaires (blessures, transactions, etc.)
- Modèles spécifiques pour différents types de paris (over/under, run line)
- Analyse des sentiments à partir des médias sociaux
- Déploiement en production avec mise à jour automatique
