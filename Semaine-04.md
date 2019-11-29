# Semaine 4 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Arnaud de Mouhy et Louis Dorard — tous droits réservés

Lecture cette semaine: fin BML et début MLY (ML Yearning)

### Lundi 14/10 (Arnaud, télé-travail): TD

* TD python :
  * argparse
  * csv
  * mysql
  * BeautifulSoup (scraping)

### Mardi 15/10

### Mercredi 16/10

### Jeudi 17/10 après-midi (Arnaud, Node): Atelier Elastic Search

* Découverte du NoSQL et d'ElasticSearch

### Vendredi 18/10 (Louis): suite projet GMSC

* Recap:
  * Elastic Search (atelier donné au Node par Matthieu Elie dans le cadre de l'aquiversaire)
    * Avantages du NoSQL: données avec structure flexible (Json), gros volumes de données
    * Recherche texte puissante
    * Intéressant pour les logs en production
    * Kibana
      * Pour se constituer un dashboard de data viz
      * Peut être utilisé aussi en dehors du stack Elastic
    * Critique: flou, survolé, partie pratique trop courte (1h, vs 2h de slides), on aimerait voir l'API Python et l'utilisation d'Elastic dans un projet
  * Outils de data viz:
    * Tableur
    * matplotlib (à venir) pour faire la même chose en code => produit une image à partir de données qui sont en mémoire
    * Dashboards construits sur D3.js avec viz dynamiques et interactives
    * plotly (à venir) pour dynamisme et interactivité, mais haut niveau comme matplotlib
    * Tableau, pour créer viz à partir de données dans une base (pas forcément en mémoire)
* Sondage: Qui a pu récupérer prédictions sur val set ou le test set?
* Envoi des prédictions sur test à [Kaggle via Python](https://github.com/kaggle/kaggle-api)
  * Dans le Dockerfile il faut rajouter l'installation de la librairie Kaggle
  * Dans la config docker compose il faut ajouter `- KAGGLE_USERNAME=xxxx` et  `- KAGGLE_KEY=xxxx` dans les variables d'environnement
* Push du code sur repo GitHub individuel
