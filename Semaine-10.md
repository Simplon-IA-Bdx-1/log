# Semaine 10 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Julien Tréguer et Louis Dorard — tous droits réservés

Lecture: Hands-on ML (Aurélien Géron)

## Lundi 25/11 (Julien)

## Mardi 26/11 (Louis)

* Migration du code GMSC sur repos créés par GitHub Classroom: démo par Nico C
  * Ajout de remote puis pull
    ```bash
    git remote add classroom (par exemple) url/de/la/remote/github/classroom
    git pull --allow-unrelated-histories classroom master
    ```
  * Merge de changements sur repo Git
  * Commit et push
* House Prices
  * Création [assignment](https://classroom.github.com/g/uVIhcKuB) et [teams](https://classroom.github.com/classrooms/57009471-promo-simplon-ia-bordeaux-1/group-assignments/house-prices) (binômes) sur Classroom
  * [Brief](https://gist.github.com/louisdorard/6d4552ff86d033e7cc8fbab82c80bf71)
* 4 sujets de veille à discuter puis présenter en groupes de 6 (ordis interdits):
  * Choix des sujets et consitution des groupes
    * Régression linéaire (Nicolas S, Pierre, Vincent, Aro, Christophe, Silvia)
    * MLP (DL Python chap. 6) (Baptiste, Mehdi, Corantin, Rachel, Maud, Guillaume)
    * Keras (DL Python chap. 7) (Rodolphe, Nicolas C, Julien, Damien, Yohan, Thibaut)
    * Mise à l’échelle des données (ML Python chap. 7) (Alexis, Laurent, Bastien, Maxime, Clément, Nicolas A)
  * [30’] Discussions de groupes, préparation restitution
  * [10'] Restitution (+ 10' questions-réponses)
* Discussion: split train-val se fait avant ou après la mise à l’échelle des données?

## Mercredi 27/11 (Louis)

* Point sur apprentissage poids et biais dans un modèle de régression linéaire
  * Idée de la descente de gradient
  * Idée de départ qui mène à l'équation normale
  * https://www.charlesbordet.com/fr/gradient-descent/#comment-lutter-contre-les-minima-locaux-
* Intervention de Fabien Durand de BigML. TODO ajouter slides.
* Démo Keras pour régression linéaire à 1 variable, sur données House Prices

## Jeudi 28/11 (Julien)

Matin: 

* Poursuite de l'atelier 2, classification d'images avec SVC/XGBoost sur 
les datasets Fashion MNIST et Hand Digits 
* Restitutions sous forme de matrice confusion 
* Mise en commun des résultats 
* Présentation d'un code exemple (Guillaume) qui montre les performances 
de SVC/XGBoost sur données brutes, sur données réduites avec PCA et 
comparaison des temps de calcul 

Après-midi:

* Introduction au Data Augmentation avec Keras 
* Utilisation de la classe de preprocessing ImageDataGenerator sur 9 
images extraites de Hand Digits avec pour objectif d'appliquer des 
shifts, rotation, extraction de features et ZCA 
* Présentation de la logique de Keras et des fonctions les plus usités 
* Reprise du notebook sur House Prices avec Keras et pistes d'évolution 

## Vendredi 29/11 (Louis)

* Résumé par Baptiste de la Conférence débat - La data : menace pour l'environnement ? https://www.facebook.com/MaisonecocitoyenneBordeaux/videos/1032697020456205/
* Discussion et veille sur le sujet IA comme aide/coût pour l'environnement
  * "Microsoft believes that artificial intelligence, often encompassing machine learning and deep learning, is a “game changer” for climate change and environmental issues." https://blogs.ei.columbia.edu/2018/06/05/artificial-intelligence-climate-environment/
  * Keynote sur le sujet "Intelligence per kilowatt-hour" à International Conference on Machine Learning 2018: https://www.youtube.com/watch?time_continue=884&v=7QhkvG4MUbk
  * https://www.linfodurable.fr/technomedias/la-pollution-invisible-du-numerique-632 
  * https://www.technologyreview.com/s/613630/training-a-single-ai-model-can-emit-as-much-carbon-as-five-cars-in-their-lifetimes/
  * https://talan.com/fileadmin/Reprise_de_contenus/siltea/Note_de_conjoncture_IA_au_service_de_la_planete.pdf
  * https://usbeketrica.com/article/l-ia-peut-elle-sauver-la-planete
  * https://www.theguardian.com/global/blog/2015/nov/13/digital-revolution-environmental-sustainable
* Présentation des veilles en 2'
  * Trouver modèle qui a un R^2 négatif (Pierre)
  * Régression linéaire - équation normale vs descente de gradient? 2 sujets à choisir:
    * Avantages / inconvénients de chaque? (Nico C.)
    * Possible d’utiliser MAPE à la place de MSE? (Silvia)
  * Impact des valeurs anormales sur la régression linéaire? (Yohan)
  * Seaborn (Nicolas S)
    * https://seaborn.pydata.org/generated/seaborn.jointplot.html
  * Illustrer le problème de “curse of dimensionality” (Christophe)
    * https://medium.com/diogo-menezes-borges/give-me-the-antidote-for-the-curse-of-dimensionality-b14bce4bf4d2
