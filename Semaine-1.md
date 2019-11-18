# Semaine 1 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Arnaud de Mouhy et Louis Dorard — tous droits réservés

### Lundi 23/9/2019 (Louis): Intro IA, use cases, Kaggle

* Exemples d’IA donnés par les apprenants
  * Assistants sur téléphone (Siri, Cortana...)
  * etc.
* Tour de table
* Intro au ML et concepts de base autour de la classification et la régression
* Exemples de use cases
  * Détection spam et emails importants
  * Prédiction prix immobilier
  * Prédiction/prévention churn
* Mini-framework pour caractériser ses use-cases (A. Contexte, B. Question à laquelle prédire les réponses, C. Collecte de données, D. Décisions - utilisation des prédictions)
  * Exercice sur la prédiction de prix immobilier
* Parcours rapide des données du challenge Kaggle [House Prices](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) avec Numbers (tableur)
* Limites de Kaggle - Vers un système intelligent qui se met à jour
  1. Récupérer données sur seloger.com ou leboncoin.fr : inputs & outputs
  2. Créer un 1er modèle prédictif
  3. 1 semaine plus tard: récupérer nouvelles données (inputs & outputs)
     1. Faire prédictions sur inputs, enregistrer prédictions
     2. Comparer prédictions aux outputs
     3. Ajouter inputs et outputs aux données d’apprentissage
     4. Créer un nouveau modèle prédictif
     5. Etc.
* Aperçu du programme: Data (Arnaud) et IA (Louis) en parallèle
  * Découvrir et maîtriser son environnement de travail (2-3 jours)
  * Initiation à la programmation via Python
  * Modules bases de données

### Mardi 24/9 (Arnaud)

* Introduction à Linux - Histoire et l'Open-Source
* Récupération du matériel informatique
* Installation des logiciels de base : [cmder](https://cmder.net), [Git For Windows](https://gitforwindows.org), Docker, VSCode, Github Desktop
* Introduction à la ligne de commande CLI
* Démonstrations combinée de VSCode, Git, cmder, vi

### Mercredi 25/9 (Louis): Evaluation ML, intro MLC

* Recap J1
  * Types de problèmes de ML
  * Limites du ML
  * Questions à se poser en 1er sur un système de ML
* Etude de cas: priority inbox (seul puis avec voisin)
  * Objectif: répondre aux emails importants plus vite et passer moins de temps dans sa boite mail
  * A. Contexte?
  * B. Question posée: "cet email est-il important?". Type de problème: classification.
  * C. Collecte des données?
  * D. Utilisation des prédictions?
  * F. Features?
* E. Evaluation: régression (MAE, MAPE) et classification (accuracy, confusion & cost matrix)
* Machine Learning Canvas pour spécifier un système intelligent
* Application du MLC sur Priority Inbox (exercice en groupes de 4, avec 1 personne de chaque "type": connaissance ML, connaissance web, connaissance maths & stats, autres)

### Jeudi 26/9: Exercice MLC

* Inauguration des locaux
* Déjeuner avec les apprenants
* Exercice: MLC sur problème de prêt bancaire (à reprendre plus tard, quand ils auront pu lire le livre sur le MLC)
  * 20' de réflexion en solo + questions
  * 10' de discussion avec voisin
  * 20' de création de son canvas en solo
* Démystifier le ML en créant des modèles prédictifs sans faire de code - démo BigML
  * Titanic
  * Visualisation des distributions des features via histogrammes
  * Création d'un arbre de décision

### Vendredi 27/9 (Louis/Arnaud): BigML sur challenge Kaggle House Prices

Matin:

* Présentation de Kaggle
  * Challenge [House Prices](http://kaggle.com/c/house-prices-advanced-regression-techniques)
  * Onglet données, pour chaque challenge: inspection via histogrammes; data_description; sample submission
  * Fonctionnement du leaderboard public et privé
* Démo BigML (suite)
  * Import des données dans BigML via URL (train et test sets)
  * Inspection du train set (histogrammes, statistiques des distributions)
  * Création d'un modèle à partir du train set
  * Création de prédictions à partir du modèle et du test set
  * Envoi des prédictions à Kaggle
* Répliquer ce qui a été montré, en binôme
* Analyse manuelle des erreurs, en solo
  * Partage du train set ("train full") en train et validation
  * Création d'un modèle sur le train et prédictions sur le validation
  * Téléchargement des prédictions et ajout de colonnes d'erreur via tableur (Pourcentage Erreur, et valeur Absolue du Pourcentage d'Erreur)
  * Calcul de MAPE
  * Tri des erreurs et inspection (sur ou sous-évaluation, features anormales, etc.)

Après-midi:

...
