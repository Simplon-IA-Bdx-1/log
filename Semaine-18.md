# Semaine 18 — formation Simplon IA à Bordeaux, promo 1

Auteur: Louis Dorard — tous droits réservés

## Mardi 10/3 (Guillaume E.)

Introduction aux principes du cloud (pay as you go, scalibility, redondance etc)
* Azure portal :
   * Notion de groupe de ressource
   * Gestion des droits sur une ressource
   * Monitoring des coûts
   * Création d’une ressource
* Azure Databricks / Spark :
   * Notion de fichier distribué (HDFS, parquet, etc)
   * Explication du fonctionnement de Spark (driver/workers, parallélisation de la puissance de calcul)
   * Notion de lazy language
* Azure Machine Learning :
   * Présentation des services cognitifs (modèles pré-entrainés) disponibles
   * Interface Azure ML Studio (datasets/experiments/modèles/endpoints)
   * Tutoriel Azure ML (https://docs.microsoft.com/fr-fr/azure/machine-learning/tutorial-train-models-with-aml)

## Mercredi 11/3 (Louis)

* Présentations entreprise:
   * Ce qu'elle fait
   * Les projets ML passés ou en cours (ou autre projets, si pas de ML jusqu'à présent)
   * Ce que vous avez fait pendant ce mois d'alternance: 
      * Votre projet
      * Les problématiques auxquelles vous avez fait face
      * Celles que vous avez résolues
      * Comment vous les avez résolues
   * Ce sur quoi vous allez travailler à votre retour en Avril:
      * Les difficultés qui restent à résoudre
      * Les pistes de résolution
* Projet immo
  

## Jeudi

Matin: projet immo
* Reprendre le projet / se refamiliariser avec:
  * Relire [Brief](https://gist.github.com/louisdorard/88e09b8fdc4be81c27cde6e1b9bb9f61)
  * Ecrire / mettre à jour README — pour Guillaume E. et Arnaud?
* Suggestions sous-projets/branches/features pour 2 personnes:
   * Script pour relancer le scrapping et l'apprentissage facilement, et créer des fichiers train-2020-01-XX.csv (pareil pour val et test) et model-2020-01-XX.pkl
   * Déploiement modèle avec Flask
   * Enregistrement des logs d'apprentissage - cf brief

Aprem:
* Présentation sujet de veille: GridSearchCV et RandomSearchCV - Maxime Yohan Rachel Coco
* Réflexion passage sous Azure:
  * BDD à mettre dans Azure? ou pas: Attention aux coûts!!
  * Scrapper avec fonction "serverless", lancée périodiquement — voir doc Azure Functions: [triggers bindings](https://docs.microsoft.com/en-us/azure/azure-functions/functions-triggers-bindings), [create scheduled function](https://docs.microsoft.com/en-us/azure/azure-functions/functions-create-scheduled-function)
