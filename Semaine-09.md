# Semaine 9 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Jean-Paul Maalouf et Louis Dorard — tous droits réservés

Louis en formation de formateurs à Montreuil. Lecture demandée: ML with Python (Brownlee), chapitres 1 à 7.

## Approcher la data science via des problématiques autres que prédictives, avec R

“Bonjour, je suis votre client. Je n’y connais rien en data. Voici un jeu de données. Faites-moi de la data science.”

* Savoir poser des questions autour d’un jeu de données brut et les traduire en questions Data Science.
* Réflexion collective sur les différentes manières de puiser de l’information à partir d’un jeu de données : statistiques univariées, bivariées, multivariées.
* Explorer plus profondément : clustering.
* Explorer plus profondément : expliquer un outcome ou comment utiliser les régressions linéaire ou logistique dans des buts explicatifs et non prédictifs.
* Mises en pratique avec R
* Projets : explorer un jeu de données en groupes de 2-3
  * Projet Chocolat
  * Projet [Fifa](https://www.kaggle.com/karangadiya/fifa19) ou Sacramento
  * Projet House Prices

## Lundi 18/11 : introduction ; outils uni et bivariés

* Construction d’un jeu de données autour des préférences de consummation de chocolat: https://docs.google.com/spreadsheets/d/11gXXZ8E1oiLWqJGjunsU5S9b1CND2CKb9HEyDm3CUug/edit#gid=328975872. Les lignes sont les élèves et les colonnes sont des questions.
* Brainstorming : votre boss ou client vous demande de faire de la data science autour d’un jeu de données (aucun objectif clair précisé, ce qui malheureusement arrive souvent). En regardant le jeu de données, quelles questions peut-on poser ?
* Classification des types de questions en 11 catégories partagées sur un google sheets. Discussion autour d’outils de visualisation / d’analyse permettant de les aborder : (onglet Questions) 

TODO formatter la table ci-dessous:

Question	Type de question	Outil 1	Outil 2	Outil 3
Quelle est la marque préférée au global ? 	Décrire 1 variable catégorielle	Compter les effectifs par catégorie (tri à plat)	Diagramme en bâtons	Mode
Comment caractériser la colonne Intensité?	Décrire 1 variable quanti	Stats Descriptives quanti (Tendance centrale comme la moyenne ; dispersion comme l'écart type)	Histogramme	
Intensité selon Age?	Lien entre 2 var. quanti	Coefficient de Corrélation	Nuage de points	
Intensité selon préférence marque?	Lien entre 1 var. quanti et 1 catégorielle	Scattergram	Diagramme en bâtons	Boxplots
Marque Préférée selon préférence Sucré/salé?	Lien entre 2 var. catégorielles	Tri Croisé (crosstab)		
Comment décrire les liens de plusieurs variables les unes par rapport aux autres? Comment décrire mon échantillon de manière synthétique et globale?	Liens multivariés	Analyse en Composantes Principales (Principal Component Analysis) ou PCA	Heatmap (visualiser matrice de corrélation volumineuse)	Graphique en araignées
Comment grouper les consommateurs en groupes de consommateurs homogènes?	Machine Learning non-supervisé (Clustering)	k-means, Classification Ascendante Hiérarchique, PAM, Clara		
Pourrait-on prédire la note d'un nouveau produit	Prédiction d'une variable quanti	Machine Learning supervisé (problématique de régression)		
Comment prédire la marque préférée ?	Prédiction d'une variable catégorielle	Machine Learning supervisé (problématique de classification)		
Quelles variables influencent au mieux la préférence du nouveau produit?	Expliquer une variable quantitative	Modèle Linéaire	Arbres de régression	Régression Ridge/Lasso (uniquement var. indépendantes quanti)
Quelles variables influencent le choix de la marque ?	Expliquer une variable qualitative	Régression logistique		

* La suite de la semaine se focalise sur toutes les problématiques autres que les 2 problématiques prédictives.
* Dans l’après-midi, degustation de After Eight et ajout d’une colonne “Note nouveau produit” au jeu de données. Objectif marketing : percer le marcher avec ce nouveau produit. 
* Exploitation des 5 premières problématiques : statistiques univariées et bivariées, introduction et ateliers sous R.

## Mardi 19/11 : problématiques uni-bivariées (suite) – problématiques multivariées (ACP)

* Ateliers uni/bivariés sur d’autres jeux de données, notamment House Prices proposé par Louis.
* En fin de journée, introduction intuitive aux problématiques d’exploration multivariées, et notamment à l’Analyse en Composantes Principales ; notions de ML supervisé vs ML non-supervisé ; ébauches de script R sur le jeu de données CRM (extraterrestres clients d’une plateforme de vente de chaussures en ligne).

## Mercredi 21/11 : problématiques multivariées (suite) - clustering

* Atelier exploratoire autour du jeu de données HousePrices (jeu de données assez challenging).
* JP montre sa manière d’aborder pas à pas l’exploration du jeu de données, réfléchit à haute voix et écrit ses réflexions, ses suppositions et sa progression tout au long du script.
* Introduction au clustering : notion de distance, Classification k-means, Classification Ascendante Hiérarchique. Ecriture de code sous R, atelier clustering sur le jeu de données Chocolat. Certains travaillent plutôt sur le jeu Fifa2019 (Kaggle).

## Jeudi 22/11 : explication d’une variable quantitative (régression linéaire) ou d’une variable catégorielle (régression logistique)

* Dégustation des Lindt apportés par Aro, et ajout d’une colonne “note Lindt” au jeu de données.
* Notion de p-value : quand p< seuil, l’effet est significatif et on est content.
* Introduction à la régression linéaire. Interprétation des coefficients ; diagnostic des résidus ; problèmes d’overfitting et de multicolinéarité (the curse of dimensionality) ; sélection de modèles.
* Atelier sur le jeu de données chocolat : On se rend compte que la préférence de Lindt est drivée par la préférence de l’aspect fourré du chocolat. La préférence de After Eight est drivée par la préférence de l’aspect intense. Discussion autour des directives marketing possibles. 
* Atelier régression autour du jeu de données HousePrices.
* Introduction-bonus à un outil de ML supervisé : KNN. Notion de hyperparameter tuning (paramètre K).
* Introduction à la régression logistique : interprétation des odds-ratio. 
* Atelier régression logistique.
* Clôture : passage en revue des 9 problématiques abordées durant la semaine.
