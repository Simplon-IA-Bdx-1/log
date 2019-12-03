# Semaine 11 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Arnaud de Mouhy, Julien Tréguer et Louis Dorard — tous droits réservés

## Lundi 2/12 (Julien)

* Présentation veille CNN en 10'

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
* House prices Keras / NN
  * Suite présentation d'un MLP à 1 couche cachée
    * Passage d'une prédiction à une valeur sur l'échelle d'origine en dollars
    * Calcul métriques de performance: MSE, RMSE sur log-prix, R^2 sur log-prix

## Vendredi 6/12 (Arnaud)

