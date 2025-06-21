Projet Data Science Supervisée – Prédiction de la variable Target
 - Objectif
Ce projet s’inscrit dans la continuité du projet NLP axé sur l’interaction conversationnelle, mais se concentre ici sur la modélisation supervisée. L’objectif principal est de prédire une variable continue Target à partir de caractéristiques individuelles, géographiques, démographiques et professionnelles.
 
Compétences ciblées
 C1 : développement, mise en œuvre et évaluation de plusieurs modèles de ML
C2 : optimisation via validation croisée et recherche d’hyperparamètres
C3 : lutte contre l’overfitting et analyse de la robustesse
 Préparation des données
 Analyse exploratoire via pandas, seaborn, corrélation, matrices de chaleur
 Catégorisation des variables (AGE_CATEGORY, DEGREE_CATEGORY, OCCUPATION_CATEGORY)
Matrice de corrélation entre les variables et la cible
Winsorization des valeurs aberrantes (sur CURRENT_AGE, TARGET)
Fusion de datasets (géographie, activité physique, population, etc.)
Nettoyage : suppression de variables non pertinentes (insee_code, noms, coordonnées brutes…)
 Regroupement de départements selon leur impact sur Target (via Kstest)
 Encodage : StandardScaler pour les numériques, OneHotEncoder pour les catégorielles
 Modèles développés
Le projet est structuré en plusieurs sous-parties correspondant aux combinaisons de variables utilisées :
- Modèle 1 : données personnelles + géographie
- Modèle 2 : géographie + emploi
 Algorithmes testés
Régression Linéaire
Random Forest Regressor
XGBoost Regressor
Tous les modèles sont :
Entraînés avec validation croisée K-Fold
Optimisés via GridSearchCV ou RandomizedSearchCV
Évalués avec :
R² (coefficient de détermination)
MAE (Mean Absolute Error)
MSE (Mean Squared Error)
 Résultats
La régression linéaire présente des limites (MSE élevé, incapacité à capturer la non-linéarité)
Le Random Forest obtient les meilleures performances avec un MSE ≈ 14
XGBoost donne aussi des résultats compétitifs tout en offrant plus de contrôle sur le biais et la variance
Conclusion
Ce projet constitue un complément algorithmique et rigoureux au projet NLP :
Permet de comparer plusieurs approches prédictives
Développe une logique d’expérimentation structurée (nettoyage, validation, tuning)
Apporte une dimension quantitative en parfaite cohérence avec les exigences du Bloc 4
