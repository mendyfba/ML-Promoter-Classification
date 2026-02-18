ML-Promoter-Classification

Ce dépôt contient un script Python (notebook) permettant de classer des séquences d'ADN procaryotes. L'objectif est de déterminer si une séquence est protrice ou non en utilisant des méthodes de traitement du langage naturel (NLP) appliquées à la génomique.

1. Approche technique
   
Le projet suit une démarche de Machine Learning classique, décomposée en étapes explicites :
Données : Utilisation du dataset "Promoter Gene Sequences" (UCI Machine Learning Repository).

Prétraitement : Nettoyage des séquences brutes et uniformisation du texte.

Tokenization : Découpage des séquences en k-mers (mots de 6 nucléotides) via une fonction personnalisée get_kmers.

Vectorisation : Transformation des mots en vecteurs numériques avec CountVectorizer (Bag of Words).

Modélisation : Entraînement d'un classifieur Random Forest pour la prédiction.

2. Contenu du dépôt
   
classification_promoteurs_ML.ipynb : Le notebook complet avec le chargement des données, l'entraînement et les tests.

Le script inclut une fonction get_kmers pour segmenter l'ADN avant l'analyse.

3. Résultats et Validation
   
Le modèle a été validé sur un jeu de test indépendant.
Précision globale : ~95% sur le dataset d'origine.
Test spécifique : Le pipeline a été testé sur la région promotrice Plac de l'opéron lactose d' Escherichia coli (gène lacZ), avec un score de confiance de 76%.

4. Outils utilisés
   
Langage : Python
Librairies : Pandas, NumPy, Scikit-learn, Matplotlib
