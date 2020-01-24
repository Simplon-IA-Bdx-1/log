# Semaine 6 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Arnaud de Mouhy et Louis Dorard — tous droits réservés

### Lundi 28/10 (Louis): suite projet GMSC

* Démos:
  * Vincent: README, commit des fichiers Dockerfile et docker-compose
  * Baptiste: structure du repo
  * Nicolas C: raccourcis clavier sur Jupyter, command palette
* Qui a committé ses fichiers csv?
  * .gitignore
  * Pas du code! On peut remplacer par le code qui permet de downloader/générer ces fichiers
  * Pas autorisé par Kaggle
  * Prend de la place
* Discussion sur MLY, en groupes (résumé chapitre par chapitre) et en classe: chacun fait un résumé aux autres, chapitre par chapitre
* Bonus projet GMSC:
  * Implémentez votre propre fonction de calcul de AUC (voir [interpretation of AUC](https://datascienceplus.com/interpretation-of-the-auc/))
  * Comparez performance de “ensemble” et de “deepnet” pour afficher des courbes (learning curves) comme à la page 11 de MLY: en abscisse, pourcentage de données de train utilisées pour créer un modèle; en ordonnée, AUC du modèle créé, sur le val set.
* Brief projet au propre: [Brief-classification-Kaggle.md](Brief-classification-Kaggle.md)

### Mardi 29/10 (Arnaud)

TODO

### Mercredi 30/10

#### Matin (Louis)

Groupes de 4

* Pédago active: Vous aussi vous êtes formateurs. Envoyez les noms de 3 personnes qui vous ont déjà aidé, ou que vous pensez qui peuvent vous aider / vous expliquer / vous débloquer. Envoyez moi les noms de 3 personnes que vous avez déjà aidé.
* Qu’avez-vous appris depuis le début? Pourquoi faisons nous ça?
  * Créez vous de nouvelles notes qui répondent à ces questions
  * Si vous séchez, regardez le brief projet classification Kaggle pour vous rafraichir la mémoire, et le log. Vous pouvez aussi lister des points que vous avez vus et dire explicitement que vous avez pas bien assimilé. Un système de notation peut être pas mal (genre '---' '--' '-' '+' '++' '+++').
  * Exemple: on a appris à exporter les 100 erreurs les plus importantes => pourquoi fait-on ça? quand?
  * Plein de choses qu’on fait qui ne servent pas à Kaggle. Par exemple, calcul du seuil optimal, plot de la learning curve…
* Prenez du temps pour alimenter vos notes perso, commencées pendant la période où on manipulait le tableur et l'interface web de BigML, avec des notes sur la période où on a manipulé Pandas et BigML via Python.

#### Après-midi (Arnaud)

TODO

### Jeudi 31/10

#### Matin (Arnaud)

TODO

#### Après-midi (Louis)

* Point sur AUC
  * Comment ça fonctionne
  * ROC -> on en parlera plus tard
  * Pourquoi calculer cette métrique?
    * Pk Kaggle le demande!
    * Pk pas besoin de vous donner une matrice de coût — quid si elle n’existe pas, ou est confidentielle
    * Pk indépendant du threshold — du coup, on retarde la question “quel est le meilleur threshold” (qui prend plus de temps à calculer que AUC)
  * Implem: éviter les boucles (cf https://engineering.upside.com/a-beginners-guide-to-optimizing-pandas-code-for-speed-c09ef2c6a4d6)
* Calcul du seuil optimal (qui maximise gain total): quelles valeurs de seuil à tester?
  * Régulièrement espacées? Combien de valeurs à tester? Pourquoi 100 pas assez? Pourquoi 100,000 trop?
  * En théorie: choisir 1 valeur de seuil entre 2 valeurs de proba consécutives
  * En pratique: les valeurs de proba sont très rapprochées aux extrêmes (en approche de 0 et 1) et plus espacées autrement; la fonction seuil -> gain total est régulière, avec un seul maximum, généralement pas trop loin de 0.5; du coup, on peut se rendre compte grossièrement de où se trouverait ce maximum, et "zoomer" à cet endroit là
