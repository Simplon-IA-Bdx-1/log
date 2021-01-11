# Semaine 28 (prévisionnel)

## Projets chef d'oeuvre

* Présentations projets: les 3 Nicolas?
* Présenter votre projet à votre binôme de réflexion. Les questions que vous vous posez. Ce que vous comptez faire en suite.

## Révisions BDD

* Démo Airtable pour prototyper BDD et logger predictions

## Révisions ML

* Rappel time series
* Bases NLP: démo [projet hotel reviews](https://deepnote.com/project/40658b92-51fb-4040-95a3-c24e90e44219#%2F01-Train-models.ipynb)
* [Eval 5](https://forms.gle/qNsoG8TPMa3yzD4w9)
  * Quels hyper-paramètres permettent de contrôler la "taille" d'un modèle de type 1) Random Forest, 2) Logistic Regression, 3) Neural Network?
    1. n_estimators, max_depth, max_features
    2. C ("inverse of regularization strength") si on utilise la pénalité L1
    3. nombre de couches et de neurones par couches
  * Dans quel cas de figure doit-on augmenter la taille d'un modèle?
    * Underfitting
  * Dans quel cas de figure appliquer de la régularisation? Citer plusieurs méthodes de régularisation.
    * Overfitting
    * Méthodes:
      * Dropout
      * Réduction de la taille du modèle
      * Enlèvement de features
      * Ajout d'une pénalité

