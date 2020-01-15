# Semaine 16 — formation Simplon IA à Bordeaux, promo 1

Auteurs: William Brojanigo et Louis Dorard — tous droits réservés

## Lundi 20/01 - Louis

* Présentation sujet de veille: API-fication d’un modèle avec Flask (librairie Python) - Nico C. Julien Silvia Damien

## Vendredi 24/01 - Louis

* Présentation sujet de veille: GridSearchCV et RandomSearchCV - Maxime Yohan Rachel Coco
* Projet immo - branches/features/sous-projets pour 2 personnes:
  * relancer le scrapping et l'apprentissage facilement, et créer des fichiers train-2020-01-XX.csv (pareil pour val et test) et model-2020-01-XX.pkl
  * déploiement modèle avec Flask
  * enregistrement des logs d'apprentissage (ex: objet history renvoyé par le fit dans Keras) et des performances de chaque modèle enregistré - dans un fichier csv ou dans une base de données - avec également toutes les infos qui ont permis de générer ces modèles (dont le hash du commit du code utilisé)
  * script pour re-générer fichiers train, val, test, modèle
