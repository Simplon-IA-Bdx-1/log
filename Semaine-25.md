# Semaine 25: renforcement — formation Simplon IA à Bordeaux, promo 1

Auteurs: Arnaud de Mouhy et Louis Dorard — tous droits réservés

## Lundi

### Où on en est

* Avril: exos nowledgeable
* Mai: DP-100
* Juin: début projets chef d'oeuvre
* Juillet: on revient sur les exercices, et on fait des renforcements

Pour le contexte, voici un message posté à la fin de la semaine d'Avril ([Semaine-22.md](Semaine-22.md)).

  Les exos sur Nowledgeable ont mis en lumière des petits points de difficulté (facilement réglables je pense, avec un minimum de travail) ou d'amélioration possible. Je vous fournis des ressources qui peuvent peut-être vous aider:

  * Gagner en rapidité sur la programmation Python. Il doit y avoir foultitude de MOOCs, mais j'aime bien ce notebook pour synthétiser la base: https://github.com/jrjohansson/scientific-python-lectures/blob/master/Lecture-1-Introduction-to-Python-Programming.ipynb Thibaud m'avait aussi parlé de ceci il y a quelques temps, pour s'entraîner sur des petits exos de difficulté variable: https://edabit.com/challenges (choisir Python).
  * Apprendre Pandas pour de vrai: on a vu certaines fonctionnalités, par nécessité, au détour des projets... Pour aller plus loin, il y a un bouquin de référence et son jeu de notebooks: https://github.com/wesm/pydata-book
  * Repréciser certaines notions de ML, autour de la performance des modèles, under et overfitting, causes possibles, que faire... -> relisez Machine Learning Yearning, là maintenant, mais aussi tous les X mois, pour se remémorer les choses.

### Points

* Projets entreprise
* Projets chef d'oeuvre
  * Qui a changé d'idée?
  * Remarque: choisir un projet avec même type d’input, mêmes outils, ou mêmes méthodos qu’en entreprise?
* Réponses au formulaire de suivi: compétences + sujets à approfondir + commentaires

### ML Katas

https://github.com/bpesquet/machine-learning-katas

* Working with data:
  * Data analysis pandas
  * Tensor management numpy
* Training models:
  * Diagnose Breast Tumors
  * Predict Housing Prices
  * Predict Heart Disease
  * Classify Flowers

Debug: performance de 0 sur le test set... 
* Quid sur le train?
* Quid si on fait un "restart + run all" du notebook?
* Si le pb persiste et que les résultats sont ok sur le train, alors c'est un problème de généralisation
* Est-il raisonnable d'espérer que le modèle généralise? Pour ça, plotter train et test et voir s'ils sont similaires.
* Où est le bug: lister tous les steps et les vérifier
  * Possible de simplifier et d'enlever certains steps optionnels, pour voir si le bug est au niveau de ces steps optionnels ou pas (par exemple: normalisation des données est optionnelle si on utilise des arbres de décision)
  * Modélisation: un test rapide consisterait à changer d'algo -> random forest
  * Standardisation: le bug typique est d'appliquer la standardisation sur le train et pas sur le test; autre bug typique: standardiser à partir de la totalité des données => fuite => résultats trop bons

## Mardi

### ML Katas

* On continue sur les katas d'hier (le 3è sur heart disease est le plus long)
* Comparaison LinearRegression et SGDRegressor: performance du modèle? temps de fit?

### Nowledgeable

* Evaluation 6 - Pandas feature engineering => présentation de Nico C

### Projet mini Kaggle API

Sur [GitHub Classroom](https://classroom.github.com/a/Lc-yG38A) - voir [brief](https://gist.github.com/louisdorard/2652fc3b53b90c8492b732b5717f49e1).

