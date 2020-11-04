# Semaine 27 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Guillaume Etchepare, Arnaud de Mouhy et Louis Dorard — tous droits réservés

## Lundi 2 novembre (Louis)

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

* Points individuels sur les projets
* Annonce de Guillaume E.: veille NLP
* Démo PyCaret par Clément
* Démo classification wolf/dog avec [img2vec](https://github.com/louisdorard/img2vec-keras/) et dabl sur [Deepnote](https://deepnote.com/project/15dfbda3-e4bf-4fa2-a7a8-c0798c16c24e)

## Mercredi 4 novembre (Louis): journée projets

Matin:
* [Eval 4](https://docs.google.com/forms/d/e/1FAIpQLSf1_DF6evrnq3thVqPCSKvxaKIPc6fFImJxsFCMvoKH_qyujg/viewform?usp=sf_link)
    * Expliquez les différents types d’overfitting qui peuvent survenir dans un projet de ML, et comment on peut les détecter. 
      * Overfitting d'apprentissage: bonne perf sur train, mauvaise sur val
        * On ajoute de la régularisation, on joue sur les hyperparamètres, afin de contrer l'overfitting d'apprentissage.
      * Overfitting de validation (quand on cherche à optimiser la pipeline):
        * Bonne perf sur val, mauvaise sur test
        * Bonne perf en cross-val sur train_full, mauvaise sur test
        * Pas besoin de regarder où on a eu des erreurs sur test! D'ailleurs il faut éviter, sinon on risque d'overfitter test...
        * Ok de regarder où on a eu des erreurs sur val, afin de générer des idées d'amélioration de collecte et préparation des données.
        * On améliore le split / on le refait d'une autre façon, pour contrer l'overfitting de validation.
    * Listez plusieurs approches pour améliorer la performance d'un modèle, par ordre de priorité, et indiquez dans quel cas de figure elles sont le plus (ou le moins) pertinentes.
      * Ajout de données, si learning curve continue de monter. De quel type? Besoin d'analyser 1er modèle, afin de savoir!
      * Amélioration de data prep: analyser prédictions pour générer des idées, puis les implémenter. Ca peut être nettoyer des features, en générer de nouvelles.
      * Changement de valeurs d'hyperparamètres, mais seulement après analyse 1er modèle, et amélioration data prep!
        * Modèle plus gros?
        * Réduire biais ou variance? (voir MLY pour comment faire; 1ère étape est de comparer performance train et val à performance désirée)
        * Recherche automatisée
    * Proposez une méthode pour quantifier à quel point le train set est représentatif du test set.
      * On regroupe les inputs des deux sets, dans un seul dataset.
      * On rajoute à ce dataset une colonne qui dit d'où vient l'input: "train" ou "test". On mélange le dataset et on considère cette dernière colonne comme output à prédire => problème de classification binaire.
      * On évalue via cross-test la performance d'un modèle simple (decision tree, qu'on peut d'ailleurs inspecter) sur ce problème. F1 meilleur que random?
  * Discussion (15')
