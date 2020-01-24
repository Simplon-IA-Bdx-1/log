# Semaine 16 — formation Simplon IA à Bordeaux, promo 1

Auteurs: William Brojanigo et Louis Dorard — tous droits réservés

## Lundi 20/01 - Louis

* Présentation sujets de veille:
  * API-fication d’un modèle avec Flask (librairie Python) - Nico C. Julien Silvia Damien
  * Ensembles et Random Forests - Thibaud Clement Alexis Rodolphe

## Vendredi 24/01 - Louis

* Présentation sujet de veille: GridSearchCV et RandomSearchCV - Maxime Yohan Rachel Coco
* Mise en commun
  * ce que vous avez appris et retirez du projet jusqu'à présent (travail équipe? git? scrapping?)
  * quantité de données collectées (biens, features)? projection sur mars? création de modèle ok?
  * groupe 1: Belles Demeures sur Gironde - immobilier de luxe - pb scrapping on est bloqués au bout d'un certain nombre de requêtes - 1500 biens et 13 features - peut-être pas bcp + de biens sur le marché d'ici mars
  * groupe 2: SeLoger sur Bordeaux et 1è périphérie en location - bloqué dès la 1è requête mais solution avec Selenium - 1150 biens en location, mais colocations à virer et 14 features - 100 de plus par semaine?
  * groupe 3: SeLoger sur Bordeaux maisons et appartements en achat avec Selenium - 847 maisons, ça mouline sur 2000 dans la liste - scrap à la volée sans stocker les pages - CSV et pas encore BDD
  * groupe 4: Green Acres simple pour scrapping, en Aquitaine - 7200 biens avec 10 features mais pas type de bien - découpé travail dès le départ, Laurent et Damien sur depo git (+ utilisation git flow) et README (suivi par le reste de l'équipe), Mehdi et Julien scrap données - fait en sorte que seules les nouvelles propriétés soient scrappées donc pas de doublon - commencé création modèle avec fichier CSV bidon - on se rend compte après coup qu'il y a des NA dans les colonnes venant du scrapping
  * groupe 5: SeLoger appartements et maisons en achat à Paris - 5000 biens avec 6 features - tous sur le scrapping au début, puis division du travail quand v1 du scrapping ok: Thibaud sur modèles, Rachel et Yohan sur scrapping; puis une fois CSV nettoyé chacun a créé un modèle - rien sur git
  * groupe 6: FNAIM Gironde scrap open bar, appartements maisons sur toute la Gironde - 3505 biens avec 4 features (script a tourné en 1 heure) - BDD sur AWS - chacun différent modèle via différents outils - surévaluent les biens?
  * mise en commun features?
* [Brief](https://gist.github.com/louisdorard/88e09b8fdc4be81c27cde6e1b9bb9f61)
* Projet immo - suggestions sous-projets/branches/features pour 2 personnes:
  * relancer le scrapping et l'apprentissage facilement, et créer des fichiers train-2020-01-XX.csv (pareil pour val et test) et model-2020-01-XX.pkl
  * déploiement modèle avec Flask
  * README pour Guillaume E. et Arnaud
  * enregistrement des logs d'apprentissage - cf brief
  * script pour re-générer fichiers train, val, test, modèle - cf brief
* Infos avant l'alternance:
  * Faire un log / journal de bord
  * Préparez présentation sur votre entreprise, pour Mars
  * Apprenez et chopez les accès aux données (ou au moins des extraits, ou un data description, ou des infos sur les quantités de données)
  * Faites de la formation interne
  * Lectures:
    * [The Machine Learning Canvas](https://gumroad.com/l/mlcanvas/gbi40xs)
    * [Datasheets for Datasets](https://www.microsoft.com/en-us/research/publication/datasheets-for-datasets/)
