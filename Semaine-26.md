# Semaine 26 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Guillaume Etchepare, Arnaud de Mouhy et Louis Dorard — tous droits réservés

## Lundi 5 octobre (Louis)

### Matin

* Tour de table: nouveautés côté entreprise et côté projet chef d'oeuvre (8 x 5')
* Révision des veilles précédentes -> MAPE - MSE, data preprocessing, métriques matrice confusion, régularisation, cross val, grid search, reproductibilité (pareil pour mardi)
* ML katas (pull updates) > [algorithms](https://github.com/bpesquet/mlkatas/tree/master/algorithms)
  * Data preprocessing
  * Classification metrics
  * Linear regression
    * Questions optionnelles:
      * "Using the normal equation, compute the theta vector that minimizes loss into the `theta_best` variable" -> vous pouvez aller directement sur "Create a scikit-learn `LinearRegression` into the variable `model`"
      * "Iterative Approach: Batch Gradient Descent"
      * Première question de "Iterative Approach: Stochastic Gradient Descent" -> vous pouvez aller directement sur "Create a scikit-learn `SGDRegressor` into the variable `model`".

### Aprem

* Katas:
  * Finir _algorithms_
  * Dans _models_ on avait déjà vu breast tumors, housing prices, heart disease, iris
  * On continue avec planar data et diabetes.
  * Il y aura aussi du temps mardi.
  * Pour ceux qui vont vite, choisissez au choix entre Images, Text et Time Series (voir https://bpesquet.github.io/mlkatas/index.html).
* Préparer présentations projets: 4-5 slides qui contiennent la problèmatique, la base de donnée avec les tables, l’approche considérée en ML... 
* Mini Kaggle:
  * Problème des indices: sont-ils conservés suite au split? à la génération du fichier de prédictions?
  * Code robuste aux prédictions dans le désordre?
  * Comment tester que ça prend bien en compte le fichier prédictions envoyé, et que ça calcule bien l'AUC?
    * Essayer avec prédictions aléatoires -> AUC devrait être de 0.5
    * Essayer avec prédictions d'un vrai modèle -> AUC devrait être 0.7-0.8
    * Essayer avec les vraies valeures d'output -> AUC devrait être de 1

## Mardi (Louis)

### Matin

* Tour de table: nouveautés côté entreprise et côté projet chef d'oeuvre
* Révision des veilles précédentes
* Suite activités de la veille.

### Aprem: optimisation hyper-paramètres

Utilisez Grid Search pour tuner les hyper-paramètres de Random Forest sur Boston Housing (dans les katas)
* Créez un notebook boston_housing_RF.ipynb
* Vous pouvez commencer ce notebook par `%run boston_housing.ipynb` (cela fait référence au kata que vous aviez déjà fait... c'est juste une suggestion!)
* Commencez avec un seul hyper-paramètre à tuner: disons max_depth. Tracez la valeur de R^2 en fonction de max_depth.
* Commit/push dans votre repo machine-learning-katas.

Utilisez Randomized Search pour tuner les hyper-paramètres de RF sur Kaggle GMSC.
* Expliquez votre stratégie d'utilisation de Grid / Randomized Search. Comment choisissez-vous l'espace à chercher / le grid?
* Quelle progression observez-vous sur votre score Kaggle?
* Commit/push dans votre repo GMSC.

