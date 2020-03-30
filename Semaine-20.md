# Semaine 20 — formation Simplon IA à Bordeaux, promo 1

Auteurs: Louis Dorard et Julien Tréguer — tous droits réservés

Télétravail cette semaine, cause Covid-19

## Lundi 23/3 (Louis)

(Pas de veille à présenter)

* Retour sur le [brief projet real-estate](https://gist.github.com/louisdorard/88e09b8fdc4be81c27cde6e1b9bb9f61)
* Questions-réponses sur le déploiement de modèles avec Flask
  * Exemple de (pseudo-)code => voir questions en commentaires

```python
from flask import Flask, request, jsonify
from joblib import load

app = Flask(__name__)

# Load model outside of prediction function, or inside?
MODEL_DATE = "20200324" # Hard-code this value, or get it from API request?
model = load("models/" + MODEL_DATE + ".joblib") # How long does it take to load model?

@app.route('/predict', methods=['POST'])
def predict():
    # Get input and make prediction
    input = request.get_json()['input']
    prediction = model.predict_proba([input])

    # Prepare result, including reference to model used
    result = jsonify(
        input=input,
        model=MODEL_DATE,
        prediction=prediction)

    # Log result before returning it to client
    with open("predict_log.txt", "a") as logfile:
        logfile.write(result)
    
    return result
```

  * Besoin (futur) de logguer quelle version de modèle a fait quelle prédiction, et de savoir recréer chaque version de modèle
  * [Doc scikit sur persistence modèle](https://scikit-learn.org/stable/modules/model_persistence.html) (voir la partie "In order to rebuild a similar model with future versions of scikit-learn, additional metadata should be saved along the pickled model")
* Finalisation projet en local
  * Point rapide d'avancement
  * Recap des sites scrappés par chaque groupe
  * Problématique de plus d'annonces (cause covid)... Quelles sont vos idées pour simuler l'arrivée de nouvelles annonces immobilières? (Sans non plus complexifier les choses niveau scrapping)
* Veille perso sur Azure ML en pratique
  * Constituez un doc. partagé pour vous aider à partager vos connaissances sur Azure et vous entraider en prévision du passage de certification

## Mardi 24/3 (Julien)

* Veille: Grid search avec time series dans scikit?! - Nico A
* Time Series
* Atelier télétravail

## Mercredi 25/3 (Julien)

Veille: Vectorisation en Python: remplacement des boucles par opérations sur tableaux + application pour tester si une série temporelle suit une marche aléatoire - Mehdi, Laurent, Damien, Alexis

## Jeudi 26/3 (Louis)

(Pas de veille à présenter)

* Matinée mise en commun: présentations de chaque groupe (10' par groupe + questions-réponses)
  * Vidéo démo de votre projet
  * Travail accompli
  * Explications du fonctionnement de votre projet
  * Votre retour d'expérience jusqu'à présent
    * Les coulisses
    * Difficultés rencontrées (et comment vous les avez résolutes)
    * Ce que vous avez appris et retirez du projet jusqu'à présent
    * Côté travail en équipe
    * Côté technique
  * Difficultés en cours et travail restant
* Idées amélioration de votre documentation, suite à la mise en commun?
* Aprem passage sous Azure


## Vendredi 27/3 (Guillaume)

Veilles:
* Exécution d’un script d’entraînement sur une **compute target** (en local, ou sur une VM basique) avec logging des métriques de performances dans Azure Machine Learning Services (AMLS) -> Maxime, Julien
* Déploiement avec **Azure Functions** (avec VS code si possible) de fonctions basiques en Python -> Nicolas S, Rodolphe
