# Semaine 19 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Louis Dorard et Julien Tréguer — tous droits réservés

Télétravail cette semaine, cause Covid-19

## Lundi 16/3 (Louis)

* Veilles:
  * DVC.org — Thibaud, Rachel
  * MLflow - Pierre, Vincent
  * Comparatif:
    * "DVC plus structuré car basé sur git" (Pierre)
    * "MLflow permet de consulter l'historique et le suivi assez facilement et rapidement" (Rachel)
    * "DVC permet de track data & experiments mais pas de déployer les modèles. Il n'a pas d'interface graphique. Du coup ça a l'air assez complémentaire si on utilise DVC juste pour la data et flow pour les modèles mais ça fait plus à apprendre." (Thibaud)
(la visualisation)
    * MLflow peut gérer des pipelines, de façon similaire à DVC (ils appellent ça un "multistep workflow"): https://github.com/mlflow/mlflow/tree/master/examples/multistep_workflow Cependant DVC a une meilleure façon de prendre en compte quels sont les fichiers créés par un "step" de pipeline/workflow et quels sont les fichiers dont ce step dépend, de sorte à ce qu'on sache quels steps il faut relancer dès qu'il y a un changement d'un des fichiers.
    * DVC peut tracker des métriques, de façon similaire à MLflow https://dvc.org/doc/command-reference/metrics#metrics Il faut pour cela un script Python qui produise un fichier json dans lequel on stocke les valeurs de métriques.
    * Les 2 outils sont complémentaires! Cherchez des articles qui parlent de l'utilisation des 2.
* Projet real-estate:
  * Point sur avancement:
    * 1 document par groupe à partager à Louis avec infos (au niveau groupe et au niveau individuel) sur
      * Ce que vous avez fait jusqu'à présent
      * Où vous en êtes
      * Ce que vous prévoyez pour la suite
    * Organisez ces infos sur les thèmes suivants: collecte de données, préparation de données, création de modèle, APIfication du modèle (possible de rajouter des thèmes ou sous-thèmes)
    * Calls avec groupes 2, 4 et 6

## Mardi 17/3 (Julien)

Veille: Exemple calcul nombre de poids et biais d'un CNN - Christophe
* Introduction aux séries temporelles
    * Définition
    * Décomposition d'une série temporelle
    * Stationnarité et test augmenté de Dickey-Fuller
    * Modèles classiques

Brief [ici](https://github.com/JTreguer/ia-bdx-ts-project1/blob/master/README.md)

## Mercredi 18/3 (Perrine)

* Exercices sur plateforme nowledgeable
* Suite projet real-estate
  * Mettez en commun et mettez au propre, avant d'aller plus loin.
  * Regardez le code fait par les autres, demandez des explications, etc.
  * Travaillez vos README

## Jeudi 19 (Louis)

* Veilles:
  * Azure Data Factory - Silvia, Bastien
  * Serverless et Azure Functions (ou autre de chez Amazon, Google, etc.) - Corantin, Nicolas C
  * Temps pour que chacun s'approprie le contenu des présentations, se documente, teste, etc.
* Suite projet real-estate
  * Calls avec groupes 1 et 3

## Vendredi 20 (Louis)

* Organisation travail à distance:
  * Moments synchrones
    * Photos à 9h, 12h30, 13h30, 17h
    * Présentations des sujets de veille entre 9h et la pause du matin
    * Point général sur l'avancement de 13h30 à 35 et de 16h55 à 17h (ou plus au besoin)
  * Moments asynchrones (possibilité de couper Teams et de vous déconnecter)
    * 2è moitié du matin -> veille en solo, sur sujets présentés par d'autres, ou sur Azure
    * Toute l'après-midi -> travail sur projet real-estate, en solo ou en binôme (pair programming)
  * Quid moments synchrones dans votre groupe, pour faire le point?
* Veilles:
  * Reproductibilité des résultats de cross_val_score quand n_jobs=-1 - Maud
  * Recall, precision, spécificité, F1 score, ROC curve — Guillaume & Yohan
* Projet real-estate:
  * Call avec groupe 5
