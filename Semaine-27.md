# Semaine 27 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Guillaume Etchepare, Arnaud de Mouhy et Louis Dorard — tous droits réservés

## Lundi 2 novembre (Louis): journée projets

Matin:
* Tour de table
* Formulaire [Suivi des compétences](https://airtable.com/shrvQOQG6PYpNzqcr) (30')
* Veille (1h):
  * [Machine Learning in action](https://bpesquet.github.io/mlhandbook/fundamentals/machine_learning_in_action.html)
  * [CRISP-ML](https://arxiv.org/abs/2003.05155) ou [ML projects guide](https://www.jeremyjordan.me/ml-projects-guide/)
  * Mise en commun
* Fin révisions avec questions évaluation: 3 fois 3 questions, 10' par question (1h30)
  * [Eval 3](https://docs.google.com/forms/d/e/1FAIpQLSegvpfS4HlNjSg15QXaYnn3whTvKmMoLb8K9SMVZkyGeHZyhQ/viewform?usp=sf_link) (30')
    * Il existe deux grands types de métriques de classification: quels sont-ils? Pourquoi utiliser un type plutôt qu'un autre?
      * Mesure de qualité de probabilité, ou de qualité de classification.
      * Utiliser qualité proba si cette dernière a besoin d'être interprétée, ou si elle sert à ranker (par ex, proba churn * revenu client). Utiliser l'autre si c'est d'une classification dont on a besoin, mais besoin d'optimiser le seuil de classif. Usuellement, on optimise la qualité des proba, puis le seuil. Si changement data preprocessing, on va directement évaluer si ça donne une meilleure qualité de classification, sans forcément évaluer la qualité de proba.
    * Citez trois métriques (ou plus) de régression. Rappelez leurs définitions, leurs propriétés, et expliquez quand utiliser l'une ou l'autre.
      * MSE: dépend de l'unité choisie (ex: prix en millers de dollars, ou en dollars); petites erreurs (<1) plus pénalisées que grosses erreurs
      * MAPE: à utiliser quand c'est l'erreur relative qui importe; ne dépend pas de l'unité; pas utilisable comme loss
      * R2: entre -infini et 1; on veut au moins 0
    * Présentez les principaux hyper-paramètres pour l'apprentissage d'un modèle de type 1) Random Forest, 2) Logistic Regression, 3) Neural Network. Regroupez ces hyper-paramètres par types:
      1. RF: arbre, ensemble
      2. LR: type de régul (l1, l2, combo des deux) et force, SGD / "solver"
      3. NN: architecture du réseau (nombre couches, neurones par couche, fonction activation, dropout), objectif à optimiser (loss et régul éventuelle), SGD (batch size, number iterations, learning rate)
  * Discussion (15')

## Mardi 3 novembre (Louis): journée projets

Matin:
* Points individuels sur les projets
* Annonce de Guillaume E.: veille NLP
* Démo PyCaret par Clément

