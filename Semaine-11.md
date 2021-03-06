# Semaine 11 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Arnaud de Mouhy, Julien Tréguer et Louis Dorard — tous droits réservés

## Lundi 2/12 (Julien)

* Présentation veille CNN en 10'
* Retour sur le notebook House Prices
    - Choix d'une variable catégorielle (bon sens)
    - Transformation de la variable catégorielle en numérique avec Pandas
    - Régression à 2 variables dans Keras, comparaison des résultats
    - Travail de préparation des données entre variables numériques et catégorielles, nettoyage des données
    - Application d'XGBoost aux données
    - Hiérarchisation des variables obtenue par XGBoost
    - Evaluation de la performance du régresseur
* Computer Vision avec OpenCV

__Traitement d'image__
  - Installation de la librairie OpenCV
  - Charger des images avec leurs couleurs ou leurs niveau de gris
  - Convertir dans différents espaces de couleur
  - Charger des images dans un répertoire, appliquer un changement de taille et sauver les images réduites
  - Essayer de segmenter des images de flammes à l'aide des couleurs

__Traitement de vidéos__

  - Charger un flux vidéo et le faire jouer dans une fenêtre (impossible depuis le docker, il a fallu passer par Anaconda en local)
  - Appliquer des méthodes de tracking incluses dans OpenCV
  - Appliquer une méthode de segmentation sémantique ([voir](https://towardsdatascience.com/object-detection-with-less-than-10-lines-of-code-using-python-2d28eebc5b11))

## Mardi 3/12 (Louis)

* [Présentation veille log-loss](https://github.com/Simplon-IA-Bdx-1/log-loss-prez/blob/master/SujetVeille_LogLoss.ipynb) en 10'
* Suite house prices Keras / NN
  * Présentation d'un MLP à 1 couche cachée
    * Passage en log output
    * Mise à l'échelle des outputs
    * Utilisation d’Adam
    * Passage des données de validation à `model.fit`
* Recap résultats Kaggle House Prices
  * 0.21 régression linéaire features numériques
  * 0.17 NN complexe sur 10 feat. num. les plus importantes (Yohan)
  * 0.14962 Random Forest / ensemble toutes features
  * 0.14494 régression linéaire avec PCA features numériques (Baptiste)
  * 0.14431 Liné-R (Yohan)
  * 0.14278 XGB toutes features
  * 0.14039 deepnet features numériques
  * 0.13843 deepnet toutes features
  * 0.12 XGB toutes features (Rodolphe)
* Problématique du travail en binôme et du merge (la plupart n'ont pas pushé récemment)
  * Conflits sur les outputs des notebooks, problématiques à gérer (Nico C.)
  * Branches? 

## Mercredi 4/12 (Arnaud)

## Jeudi 5/12 (Louis)

* Présentation veilles en 2'
  * One-hot encoding pour transformer du catégoriel en binaire: avec Pandas (get_dummies) et scikit-learn (Vincent)
  * Créer une fonction sigmoïde en Python, et faire un plot (pour vérifier qu’elle est sigmoïde) (Guillaume)
  * Pourquoi features corrélées posent problème à la régression linéaire? (Julien)
  * Gradient Descent, Mini-batch GD, Stochastic GD: quelles différences? (Rachel)
  * 2 neurones entrée, 1 neurone sortie, 2 couches cachées de 3 neurones: combien de paramètres à apprendre? (coefficients et biais) (Laurent)
  * Avantages / désavantages d’initialiser tous les poids à 0? (Rodolphe)
  * Visualiser comportement de rescale, standardize, etc., sur jeux de données de votre choix (réel ou fictif) - par exemple, comment ça se passe avec les outliers? (sans vous limiter à ça non plus) (Damien)
* Log de la formation (ce document, et les autres!)
* House prices Keras / NN
  * Présentation Rodolphe XGB House Prices; mention des ensembles de modèles
  * Présentation Yohan MLP; mention de nouvelles options pour `kernel_initializer` et `optimizer` qui donnent de meilleurs résultats sur house prices
  * Présentation Pierre suppression outliers
  * Suite présentation d'un MLP à 1 couche cachée
    * Passage d'une prédiction à une valeur sur l'échelle d'origine en dollars
    * Calcul métriques de performance: MSE, RMSE sur log-prix, R^2 sur log-prix
  * Démo BigML pour trouver une bonne architecture de NN, et répliquer sur Keras
  * (Re-)lecture [brief](https://gist.github.com/louisdorard/6d4552ff86d033e7cc8fbab82c80bf71), en particulier _Livrables_ et _Evaluation_
  * Objectif semaine prochaine: finaliser projet, et améliorer le code pour faciliter:
    * reproductibilité des résultats
    * tests de différentes combinaisons de valeurs d'hyperparamètres
    * déploiement en production et prédictions sur 1 seule nouvelle input
* Travail pour le week-end:
  * Relire le référentiel de compétences, pour faire le lien avec les compétences visées par les projets
  * Se former sur les branches Git: création, merge, pull request, etc., pour savoir collaborer avec votre binôme
  * Finaliser GMSC si besoin, pour se mettre en mode "finalisation" avant les vacances (voir [brief](https://gist.github.com/louisdorard/459f65419c078c38ceb4802c9bb3ba8c), et en particulier _Livrables_ et _Evaluation_)

## Vendredi 6/12 (Arnaud)

