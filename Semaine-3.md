# Semaine 3 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Arnaud de Mouhy et Louis Dorard — tous droits réservés

### Lundi 7/10: reprise projet GMSC avec outils Python

#### Révisions

* Pourquoi on fait les choses dans cet ordre (évaluer performance, et préparer les données, en 1er!).
* Autres outils graphiques que BigML: Azure ML Canvas (SaaS); DataRobot, H2O (à installer).
* A venir:
  * Fonctionnement arbre de décision (1-click decision tree)
  * Fonctionnement random forest (1-click ensemble)
  * Fonctionnement modèle linéaire
    * Somme (pondérée) / soustraction de features : pas utile pour modèles linéaires, mais plus utile pour arbres de décision
  * BigML via Python
* Tableurs
  * Comment remplacer des valeurs, sur juste une colonne?
  * Fonction IF / SI
  * Comment faire une formule? Comment l’appliquer? Comment fixer les références à certaines lignes/colonnes/cellules?
  * Où est la liste des fonctions? comment fonctionne l’aide?
* Evaluation et split des données
  * Pourquoi restrictions sur évaluations Kaggle
  * Possibilité de sur-apprentissage dans la sélection de modèles
  * On fait les transformations sur le dataset train, puis sur val et sur test, ou sur train_full, puis sur test?

#### Conteneur Docker handson-ml

* Deux possibilités pour le mettre en place:
  * faire un build
  * décompresser le zip fourni par Baptiste puis ajouter l'image via ```docker load -i handsonml.docker```
* Log into docker container: deux possibilités
  * Bouton dans Kitematic
  * ```$ docker exec -it handson-ml bash```
* Installer des nouvelles librairies dans ce conteneur (éphémère)

  ```bash
  sudo su root
  pip install bigml
  ```

* Commentaires du Dockerfile et ajout de "pip install" à la fin du fichier

  ```Docker
  USER root
  RUN pip install "bigml"
  ```

* Fichier Docker compose et modifications
  * Changer "volumes", par exemple ../../ au lieu de ../
  * Changer "command" pour ne plus demander mot de passe:
    > /opt/conda/bin/jupyter notebook --ip='0.0.0.0' --port=8888 --no-browser --NotebookApp.token='' --NotebookApp.password=''
  * Ajout de variables d'environnement:

    ```yaml
    environment:
      - BIGML_USERNAME=...
      - BIGML_API_KEY=...
    ```

* > docker-compose up
* Risques de ne pas avoir un mot de passe sur jupyter notebook

#### Python

* Notebooks
  * Intro Jupyter
  * Pandas
    * Intro notebook
    * 10 minutes to Pandas
* [Wrappers BigML pour Python](https://bigml.readthedocs.io/en/latest/)

#### Exercice (pair programming): reprendre exercice de la semaine précédente, via Python

* Commencez par pseudo code
* Vérifiez que vous obtenez les mêmes résultats sur Kaggle
* Astuces:
  * Téléchargez le résultat du split (train et val) depuis BigML, sur vos machines, plutôt que de faire le split avec Python (1 problème de moins)
  * Possibilité d'inclure un bloc ```!pip install bigml``` en début de notebook

### Mercredi 9/10 (Louis): révisions et suite project GMSC

* Révisions en groupes de 4
  * [Schéma récap manips sur BigML](https://docs.google.com/drawings/d/1kuv4cdKUQHOz6YqKrz56b_RC_CIe96UzS6-TlVCnj8M/edit)
  * [Schéma Cycle Data](https://drive.google.com/drive/u/1/folders/1BNa1kF5MySWmoKDJVjnlT-aqNKh7e7Fs)
  * [Notes de Rodolphe](https://drive.google.com/drive/folders/12_BtLKdlKLFZth4HOILPBGjfyFfljSgN)
  * [Code de Guillaume (Github)](https://github.com/guitoo/ML-notebooks/)
* Suite exercice en binômes
* Télétravail (après-midi)
