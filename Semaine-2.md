# Semaine 2 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Arnaud de Mouhy et Louis Dorard — tous droits réservés

Lecture demandée cette semaine: Bootstrapping Machine Learning

### Lundi 30/9 (Arnaud)

* Docker BDD?
* [Aide mémoire](https://sql.sh/ressources/document/mysql-aide-memoire-sql.pdf)

### Mardi 1/10 (Arnaud)

* Docker Python+Jupyter (image de Hands-on ML)

### Mercredi 2/10 (Louis): révisions + analyse des erreurs + mise en pratique avec BigML sur Kaggle House Prices et Give Me Some Credit

* Recap des 3 journées de la semaine précédente
* Cette semaine: on continue sur BigML, via interface graphique, et enfin via Python
* Ensuite, on programmera en Python une partie de ce qu’on fait actuellement sous Excel

#### Retour sur le MLC

Compétences touchées par le MLC (voir [référentiel](https://docs.google.com/document/d/1BjNwGGX6ZaIWrwEf4Bn72tW0CbJiqqWp_XSUL_SypTQ/edit)):

* Transverses:
  * C8. "Analyser et formaliser la demande ou le besoin en développement et en exploitation de base de données"
  * C9. "Autocontrôler, tout au long du processus de développement, la cohérence des données et la conformité à la demande"
  * C10. "Suivre, adapter et rendre compte de la réalisation du projet à partir du planning projet validé" => le MLC permet d’établir / affiner le planning projet
* C12. "Constituer un jeu de données exploitable de manière à entraîner un modèle d'apprentissage en utilisant la méthodologie et/ou l'outil approprié en fonction des standards de l'écosystème" => collecte de données et features
* C14. "Exploiter un modèle d’apprentissage supervisé ou non supervisé permettant la classification ou la prédiction d’une variable en fonction des données disponibles et des outils sélectionnés" => réfléchir aux contraintes techniques sur les prédictions à faire faire au modèle
* C15. "Améliorer les performances d’un modèle d’apprentissage à l’aide d’une évaluation de la qualité des données et de la technique de modélisation afin de réduire les biais et les anomalies de résultats" => parties évaluation (offline et live)
* C19. "Développer une application et/ou des fonctionnalités utilisant le traitement de données généré par l’IA de manière à être exploitable par le client/utilisateur final" => on considère comment les prédictions vont être utilisées et vont impacter l'utilisateur final

#### Retour sur le split train-validation-test

Kaggle ne montre pas l’output du test set, garde secret le private leaderboard, et ne permet pas plus de 10 submissions par jour — pourquoi?

L’intérêt du validation set est de...

* Sélectionner meilleurs choix de préparation de données (remplacement valeurs manquantes? nouvelles features?) et de modélisation (ensemble? deepnet? quels paramètres?) en regardant ce qui donne les meilleurs résultats d’évaluation sur le val set
* Inspecter le comportement du modèle en comparant, sur le val set, la prédiction à la vraie output (qui n’est pas connue sur le test set)

Autres remarques sur le split:

* Compute performance metrics on a baseline (could be human, or a simple heuristic, or a hand-crafted rule)
* Time component could be hidden, e.g. priority inbox
  * Some features are using information from the past, e.g. how many previous important emails from the sender.
  * You can't do a random split! Can you guess why?
  * Let's say we only have 2 emails, from the same sender: in chronological order, email_1 and email_2.
    * email_2 is in training and says that previous emails from this sender were important
    * email_1 is in test
  * I have information on the output of email 1 in my training set
  * Need to do a linear split
* Think of evaluation as a simulation!
* Test set should be large enough for results to have meaning in the domain of application
  * Imagine you're modeling behavior that has a yearly pattern, e.g. sales
  => have at least 1 year in test
  * Imagine you're planning to use the same model for X days
  => have X days in test
* Beware [data leakage](https://machinelearningmastery.com/data-leakage-machine-learning/)
* Stratified Split, pour s'assurer qu'il y a la même distribution d'output en validation qu'en training (exemple où il y a 98 éléments de la classe A et 2 éléments de la classe B, à splitter)

#### Inspection globale d'un modèle

* Partagez vos MAPE sur le val set, en précisant votre type de modèle (arbre de décision, régression linéaire, ou deepnet)
* Baseline: mean regressor. Pire ou meilleur que régression linéaire?
* Feature importances
* Partial Dependence Plots: see [BigML documentation](https://static.bigml.com/pdf/BigML_Classification_and_Regression.pdf?ver=79eb166)

#### Analyse manuelle des erreurs sur house prices (suite)

* Partagez vos remarques en MP sur Discord, avec id du bien, prédiction obtenue, type de modèle, et interprétation/recommandation
* Présentation au tableau de ce que vous avez trouvé

#### Détection d'anomalies

* Démo détection d'anomalies: apprentissage non supervisé, score d'anomalie, explication
* Intégrer scores d'anomalie dans l'analyse manuelle des erreurs sur le val set, et explications du score de chaque input
* Continuer analyse manuelle des erreurs

#### Classification

* Rappel classification: définition FP et FN, matrice de confusion
* Baseline: mode classifier & random classifier
* Démo BigML pour télécharger probabilité de classe Positive sur challenge [Give Me Credit](https://www.kaggle.com/c/GiveMeSomeCredit/)
  * Données de train sur https://oml-data.s3.amazonaws.com/kaggle-give-me-credit-train.csv

### Jeudi 3/10 (Louis): début projet Give Me Some Credit: préparation des données et analyse de modèle via interfaces graphiques

#### Recap

* Baselines
  * Classification -> random classifier, mode classifier
  * Régression -> mean regressor
* Split des données
  * Vérifier et conserver les proportions de classes (ex: 94% A, 6% B) de train_full à train et val
  * Split linéaire dans le temps, quand il y a un composant temporel (caché) (ex: features construites sur emails reçus par le même expéditeur dans le passé)
* Analyse modèle entraîné sur train set
  * Comportement global
    * Feature importances
    * PDP
  * Comportement sur val set
    * Télécharger les prédictions (pour régression) ou probabilités de classe positive (pour classification binaire)
    * Créer colonne erreurs
    * Calculer mesures d’erreurs agrégées (classification: FP, FN; régression: MAPE)
    * Trier données de validation par erreur décroissante et inspecter individuellement les plus grosses erreurs

#### Exercice en binôme

Préparer un modèle pour avoir les meilleurs résultats possible sur Kaggle Give Me Some Credit

* Formulez votre idée (par ex: remplacer valeurs manquantes ou aberrantes)
* Mettez en application sur les train et val sets => train_idee_X et val_idee_X
* Créer un nouveau modèle model_idee_X à partir de train_idee_X
* Analysez model_idee_X
  * Comportement global
  * Comportement sur val_idee_X
* Vérifiez qu’il y a amélioration grâce à votre idée. (Parfois vous verrez une réduction sur le nombre de FN, au détriment de nouveaux FP: inspectez les nouveaux FPs!)
* Priorisez vos prochaines idées de préparation des données à mettre en place, en se basant sur l’analyse des erreurs, ou formulez de nouvelles idées d’amélioration
* Quand vous vous sentez prêts, préparez des prédictions sur le test set et envoyez les à Kaggle. Que le meilleur gagne!

##### Idées sur les valeurs manquantes ou aberrantes

* MonthlyIncome manquant à remplacer par 0
* DebtRatio aberrant à remplacer par …

##### Idées sur les features à créer

Pê pas toutes pertinentes:

* Additionner NumberOfTimes90DaysLate, NumberOfTime60-89DaysPastDueNotWorse et NumberOfTime30-59DaysPastDueNotWorse?
* Créer une feature “Monthly_balance”, qui soustrait monthly debt à monthly income?
* Créer une feature “Income_per_person” qui divise le monthly income par le nombre de personnes à charge? ou une feature Balance_per_person?
* NumberOfOpenCreditLinesAndLoans semble être toujours plus élevé que NumberRealEstateLoansOrLines… créer NumberCreditLines qui serait la soustraction des deux?
* Créer une feature "Debt", à partir de "DebtRatio".

Faire les changements sur train_full ou train?

##### Démos

* Matrice de gain et calcul du gain total
* Il est possible d’analyser les erreurs sans passer par FP et FN:
  * Tri des données par Proba Positive décroissante: a-t-on, sur la colonne SeriousDlq, tous les 1 en haut et les 0 en bas?
  * Idem si tri croissant: a-t-on tous les 0 en haut et les 1 en bas?
* Fonctionnalité d'évaluation sur BigML
* AUC: interprétation

Voir feuille de calcul: [Give Me Some Credit: Predictions on 20% validation set of 1-click ensemble trained on remaining 80%](https://www.icloud.com/numbers/0vPSoAx87Mbbl106yMsvc9E1w#Predictions_give_me_some_credit)

### Vendredi 4/10 (Louis): partage idées sur projet GMSC + suite + points individuels avec apprenants

Petit récap de ce qui a été montré ce matin par Mehdi et Nicolas:

* Remplacement valeurs manquantes
  * MonthlyIncome et autres features: NA -> 0 (faire rechercher remplacer dans Excel)
* Ajouts de features
  * isOld: 1 si plus de 70 ans
  * MonthlyDebt
  * MonthlyBalance
  * NumberOfTimes30DaysOrMoreLate: super importante
  * ratioIncomeDependents

Formules:

* MonthlyDebt = DebtRatio * MonthlyIncome
* MonthlyBalance = MonthlyIncome - MonthlyDebt
* isOld = SI(age>=70;1;0)
* NumberOfTimes30DaysOrMoreLate = somme(NumberOfTime30-59DaysPastDueNotWorse;NumberOfTime60-89DaysPastDueNotWorse;NumberOfTimes90DaysLate)
* ratioIncomeDependents = MonthlyIncome/(NumberOfDependents+1) (ici on aurait pu utiliser le MonthlyBalance à la place de MonthlyIncome)

Damien a montré la création d’une colonne MonthlyDebt: les valeurs aberrantes de DebtRatio semblent être des valeurs de dette mensuelle en dollars.

Valeurs aberrantes de DebtRatio?

Résultats Kaggle:

* Julien et Vincent: 0.85817
* Corentin: 0.85640 sans OptiML et 0.86380 avec
* Rodolphe: 0.86584 (avec OptiML et Fusion)
* Guillaume et Laurent: 0.86057
* Mehdi et Nico: 0.85953
