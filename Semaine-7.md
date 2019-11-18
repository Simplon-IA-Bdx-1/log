# Semaine 7 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Arnaud de Mouhy et Louis Dorard — tous droits réservés

### Lundi 4/11 (Louis)

* Learning curves sur GMSC
  * Implémentation
    * Présentation par Vincent (travail effectué avec Bastien) sur comment ils ont fait pour afficher learning curve
    * Sélection des x% des premières lignes d'un dataframe
    * Utilisation de [arange](https://docs.scipy.org/doc/numpy/reference/generated/numpy.arange.html)
    * Enregistrement des valeurs d'évaluation: sous format CSV (avec `to_csv` de Pandas), ou en utilisant [pickle](https://docs.python.org/3/library/pickle.html) ou joblib pour sérialiser des objets Python

      ```python
      from joblib import dump
      dump(model, 'my_model.joblib')
      ```

      ```python
      from joblib import load
      model = load('my_model.joblib')
      ```

    * Documentation des fonctions Python (voir [PEP Style Guide](https://www.python.org/dev/peps/pep-0008/#documentation-strings) et [Sam & Max — Les docstrings en Python](http://sametmax.com/les-docstrings/))
  * Comparaison deepnet et ensemble
  * Analyse biais / variance, en comparant performance sur train, val, et performance désirée (le meilleur score Kaggle)
    * Deepnet a un biais important
    * Ensemble a une variance plus importante que deepnet
  * Exercice: moyenner les learning curves dans votre groupe pour éliminer l'effet du validation set
Il faut effectivement s'aligner sur quelles valeurs vous calculez, i.e. tous les 10% de training set, ou tous les 5%
Faites en autant que vous voulez, mais assurez vous au moins de faire 10%, 20%, 30%... jusqu'à 100% (donc 10 valeurs)
  * Moyenne des [résultats de tout le monde](https://docs.google.com/spreadsheets/u/1/d/1XuezFZKoyRtHubATAl1nIZkhrcRa_s9dN2qbhoOe1Sg/edit?usp=drive_web&ouid=115265639304725013273) dans le but d'éliminer l'effet du choix du val set sur la learning curve
    * Affichage des écart-types (voir [Visualizing Errors](https://jakevdp.github.io/PythonDataScienceHandbook/04.03-errorbars.html) dans Python Data Science Handbook)
* Utiliser scikit ou XGBoost à la place de BigML
* Démo RISE, pour présenter notebooks en mode slides
  * Pour préparer les slides: "View > Cell toolbar > Slideshow"
Installer RISE en rajoutant une ligne rise à requirements.txt
* Mise en commun dans chaque groupe de 4
  * Code
    * Kaggle: synchronisez vos résultats. Partagez vous vos résultats sur Kaggle. Qui a les meilleurs résultats, par groupe? Essayez de comprendre pourquoi vos résultats sont inférieurs.
    * Pour info, après il y aura un exercice / mini-projet individuel
    * Commit push!
  * Notebooks à mettre au propre, avec explications et commentaires
    * Pensez rapport
    * Commit push!
  * Notes
    * Listes de ce que vous avez appris (que vous m’aviez envoyées)
    * Discutez entre vous des points sur lesquels vous êtes moins sûrs
    * Notes pour faire le lien entre les éléments de cette liste, et le code
    * Entre autres: récapitulatif méthodo Kaggle (1 par groupe)

### Mercredi 6/11 (Louis)

* Reprise de la mise en commun (features, modèle choisi — BigML ou RandomForestClassifier ou XGBoost)
* Récap méthodo Kaggle
* Démos
  * Outils divers
    * Diff dans GitHub Desktop
    * Diff de notebook avec [nbdiff](https://github.com/tarmstrong/nbdiff)
    * Extension Table of Contents - [plus d'infos sur les extensions Jupyter](https://towardsdatascience.com/bringing-the-best-out-of-jupyter-notebooks-for-data-science-f0871519ca29)
      * Rajouter `jupyter_contrib_nbextensions` à `requirements.txt`
      * Rajouter `RUN jupyter contrib nbextension install` à la fin du Dockerfile
      * Committer requirements et Dockerfile
    * [Papermill](http://papermill.readthedocs.io): `papermill Credit-Model-Create-sklearn.ipynb output.ipynb`
    * Dans VS Code:
      * Live Share
        * Ajouter Extension
        * Sign in - astuce user code
      * Nouvelle vue notebooks
      * "Save as Python script"
  * `train_test_split` avec sklearn, et concept du seed
  * Seed dans BigML

### Jeudi 7/11

#### Aprem (Louis)

* Retour sur learning curve:
  * Sens de la moyenne des learning curve? Sachant qu’on n'a pas la même préparation de données
  * Démo Guillaume (avec `fill_between`)
  * Démo Aro
* Méthodo Kaggle: prez de chaque groupe
* Exercice individuel: création de prédiction sur un seul input.
  * L’application utilisée par le banquier nous envoie les informations suivantes:

    ```json
    {
        "RevolvingUtilizationOfUnsecuredLines": 0.01703559,
        "NumberOfDependents": 1,
        "DebtRatio": 0,
        "age": 42,
        "NumberOfOpenCreditLinesAndLoans": 6,
        "NumberRealEstateLoansOrLines": 1,
        "NumberOfTime30-59DaysPastDueNotWorse": 1,
        "NumberOfTime60-89DaysPastDueNotWorse": 0,
        "NumberOfTimes90DaysLate": 0
    }
    ```

  * Créez un nouveau notebook, dans lequel vous calculerez une probabilité de défaut de remboursement.
  * Committez et partagez le lien
