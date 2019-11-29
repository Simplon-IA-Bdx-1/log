# Semaine 5 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Arnaud de Mouhy et Louis Dorard — tous droits réservés

Lecture cette semaine: MLY pour tout le monde, chapitres 1 à 19

### Lundi 21/10 (Arnaud): Python

* Correction du TD de la semaine 4
  * pratique du python avec les modules argparse et csv
  * Utilisation de git

### Mardi 22/10 matin (Arnaud)

* Webscraping python avec BeautifulSoup, sur fr.wikipedia.org

### Mercredi 23/10 (Arnaud)

* Webscraping python avec BeautifulSoup, sur imdb.com
* Découverte du débugger VSCode (breakpoints, execution temps-réel)
* Nouvelle explication sur git
* Introduction très rapide sur la programmation objet

### Jeudi 24/10 (Louis): suite projet GMSC

En groupes de 4

* Sondages:
  * Quelles difficultés rencontrées?
  * Qui a la même chose que BigML?
  * Qui a calculé la matrice de confusion sur le val set?
  * Qui a fait faire des évaluations à BigML et récupéré les métriques de performance calculées par BigML?
  * Qui a pu obtenir les mêmes résultats que précédemment sur Kaggle? Ou meilleurs? -> Moins de 5 personnes
* Analyse erreurs sur le val set, avec Pandas:
  * Construction colonne erreurs
  * Calcul du nombre de vrais/faux positifs/négatifs, accuracy, et comparer avec ce que donne BigML
  * Exporter les 100 plus grosses erreurs, pour analyse dans Excel
* Améliorations docker:
  * Installation librairies dans Dockerfile via fichier requirements
  * Déplacement des variables d'environnement du `docker-compose.yml` vers un fichier `auth.env` séparé

### Vendredi 25/10 (Louis): suite projet GMSC

* Suite exercice / projet:
  * Finir analyse erreurs sur val set
  * Trouver seuil qui optimise le gain total sur le validation set, via « threshold validation set », pour la matrice de gains/coûts suivante:

  Actual / Predicted	0	1
  0	$500	-$500
  1	-$2500	$0

  * En binômes
    * Expliquez vous où vous en êtes et ce que vous comptiez faire ensuite. Faites exercice ensemble sur une des machines
    * Implémentez la même solution sur l’autre machine

* Point d'avancement dans la formation
  * Refaire avec Python ce qu’on a fait... Que reste-t’il?
  * Traiter house prices avec Python!
    * Création modèle
    * Analyse erreurs
  * Des choses qu’on a fait sur give me credit mais pas sur house prices?
    * Préparation des données -> nouvelles features
    * Envoi à Kaggle
  * Comprendre fonctionnement "1-click ensemble" et "1-click deepnet"
  * Traiter problèmes de classification où inputs sont des images ou du texte
* Démos:
  * Nicolas S / Guillaume
  * Laurent / Corantin
  * Bastien / Maud
  * Aro / Alexis
  * Julien / Bastien
* Rappel: envoi de vos notes sur MLY
  * Lien vers vos notes ou fichier notes
  * Lien vers un PDF annoté, ou vers annotation summary, ou fichier
