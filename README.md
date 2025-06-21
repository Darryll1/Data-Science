#  Projet Data Science Supervisée – Prédiction de la variable Target

##  Objectif

Ce projet s’inscrit dans la continuité d’un projet NLP orienté interaction conversationnelle. Ici, l’objectif est de développer une approche **de machine learning supervisée** pour prédire une **variable continue `Target`**, à partir de caractéristiques :

- Individuelles  
- Géographiques  
- Démographiques  
- Professionnelles

---

##  Compétences ciblées

- **C1** : Développement, mise en œuvre et évaluation de plusieurs modèles de ML  
- **C2** : Optimisation via validation croisée et recherche d’hyperparamètres  
- **C3** : Lutte contre l’overfitting et analyse de la robustesse  

---

##  Préparation et traitement des données

- Analyse exploratoire (`pandas`, `seaborn`, matrices de corrélation)
- Catégorisation :
  - `AGE_CATEGORY`
  - `DEGREE_CATEGORY`
  - `OCCUPATION_CATEGORY`
- **Winsorization** des outliers sur `CURRENT_AGE` et `TARGET`
- Fusion de jeux de données (géographie, activité physique, population…)
- Nettoyage : suppression de variables non pertinentes (`insee_code`, noms, coordonnées brutes…)
- Regroupement des départements selon leur impact sur `Target` (test de Kolmogorov–Smirnov)
- Encodage :
  - `StandardScaler` pour les variables numériques
  - `OneHotEncoder` pour les variables catégorielles

---

##  Modèles développés

Deux structures de jeux de données ont été testées :

- **Modèle 1** : Données personnelles + géographie  
- **Modèle 2** : Géographie + emploi  

###  Algorithmes utilisés

- Régression Linéaire  
- Random Forest Regressor  
- XGBoost Regressor  

Tous les modèles sont :

- Entraînés avec validation croisée **K-Fold**
- Optimisés avec **GridSearchCV** ou **RandomizedSearchCV**
- Évalués avec les métriques suivantes :
  - Coefficient de détermination **R²**
  - Erreur absolue moyenne **MAE**
  - Erreur quadratique moyenne **MSE**

---


##  Conclusion

Ce projet permet de :

- Comparer plusieurs approches de modélisation supervisée
- Appliquer des techniques rigoureuses de prétraitement, d’expérimentation et de tuning
- Apporter une dimension prédictive complémentaire au projet NLP, en ligne avec les attentes du **Bloc 4** (modélisation, rigueur, performance)

---

 _Le code source, les notebooks et les visualisations sont disponibles dans ce dépôt._
