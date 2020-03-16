# Semaine 16 — formation Simplon IA à Bordeaux, promo 1

Auteurs: William Brojanigo et Louis Dorard — tous droits réservés

## Lundi 20/01 - Louis

* Présentation sujets de veille:
  * API-fication d’un modèle avec Flask (librairie Python) - Nico C. Julien Silvia Damien
  * Ensembles et Random Forests - Thibaud Clement Alexis Rodolphe

## Mardi 21/01 - William

* Analyse de la fréquence des mots : présentation du contexte
* La lemmatisation : concepts et application avec TreeTagger
* Les stopwords : concepts et traitements
* Application pratique (en groupe) : articles de presse en plusieurs langues
* Présentation de l’analyse faite par chaque groupe

## Mercredi 22/01 - William

* L’analyse des sentiments : présentation du contexte
* Application d’un lexicon : FEEL, la librairie R rfeel et la méthodologie appliquée chez 10h11
* Application pratique (en groupe) : articles de presse en français
* Présentation de l’analyse faite par chaque groupe
* BONUS : fake articles et application pratique avec les chaînes de Markov (sans rentrer dans l'algorithme, ni dans le code)

## Jeudi 23/01 - William

* Text Classification : présentation du produit 10h11 “Social Passenger” et de la méthodologie appliquée
* Focus : la génération d’un dataset d'apprentissage
* Application pratique (1) : labellisation (individuel) des tweets en fonction de la tonalité, l’ironie et pub/presse
* Application pratique (2) : en groupe, comparaison des labellisations et identification des tweets les plus en désaccord, présentation des résultats

## Vendredi 24/01 - Louis

* Création comptes Azure. Quelques remarques:
  * Possible d'utiliser Azure ML Studio, sans crédit, et sans avoir eu à donner sa CB. Peut-être d'autres produits Azure également.
  * Crédit offert pendant 1 mois, a priori seulement si on donne sa CB
  * Attention à "annuler" / retirer la CB dans 1 mois, pour ne pas être facturé
  * Gardez un oeil régulièrement sur votre consommation, au cas où vous épuiseriez plus rapidement que prévu le crédit gratuit — sinon vous allez devoir payer!
* Projet immo
  * Mise en commun
    * ce que vous avez appris et retirez du projet jusqu'à présent (travail équipe? git? scrapping?)
    * quantité de données collectées (biens, features)? projection sur mars? création de modèle ok?
    * groupe 1: Belles Demeures sur Gironde - immobilier de luxe - pb scrapping on est bloqués au bout d'un certain nombre de requêtes - 1500 biens et 13 features - peut-être pas bcp + de biens sur le marché d'ici mars
    * groupe 2: SeLoger sur Bordeaux et 1è périphérie en location - bloqué dès la 1è requête mais solution avec Selenium - 1150 biens en location, mais colocations à virer et 14 features - 100 de plus par semaine? - BDD gratuit avec https://remotemysql.com
    * groupe 3: SeLoger sur Bordeaux maisons et appartements en achat avec Selenium - 847 maisons, ça mouline sur 2000 dans la liste - scrap à la volée sans stocker les pages - CSV et pas encore BDD
    * groupe 4: Green Acres simple pour scrapping, en Aquitaine - 7200 biens avec 10 features mais pas type de bien - découpé travail dès le départ, Laurent et Damien sur depo git (+ utilisation git flow) et README (suivi par le reste de l'équipe), Mehdi et Julien scrap données - fait en sorte que seules les nouvelles propriétés soient scrappées donc pas de doublon - commencé création modèle avec fichier CSV bidon - on se rend compte après coup qu'il y a des NA dans les colonnes venant du scrapping
    * groupe 5: SeLoger appartements et maisons en achat à Paris - 5000 biens avec 6 features - tous sur le scrapping au début, puis division du travail quand v1 du scrapping ok: Thibaud sur modèles, Rachel et Yohan sur scrapping; puis une fois CSV nettoyé chacun a créé un modèle - rien sur git
    * groupe 6: FNAIM Gironde scrap open bar, appartements maisons sur toute la Gironde - 3505 biens avec 4 features (script a tourné en 1 heure) - BDD sur AWS quasi gratuit (Rodolphe) - chacun différent modèle via différents outils - surévaluent les biens?
    * mise en commun features
  * Temps pour (re)faire ce que vous n'aviez pas eu le temps - ex: scrapping, BDD
  * Déploiement modèle avec Flask
* Infos avant l'alternance:
  * Faire un log / journal de bord
  * Préparez présentation sur votre entreprise, pour Mars
  * Apprenez sur l'entreprise / l'équipe / le projet et récupérez les accès aux données (ou au moins des extraits, ou un data description, ou des infos sur les quantités de données)
  * Faites de la formation en interne
  * Lectures:
    * [The Machine Learning Canvas](https://gumroad.com/l/mlcanvas/gbi40xs)
    * [Datasheets for Datasets](https://www.microsoft.com/en-us/research/publication/datasheets-for-datasets/)
  * Si vous avez le temps pendant l'alternance: préparez un README du projet immo pour Guillaume E. et Arnaud
