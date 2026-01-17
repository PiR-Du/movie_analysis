# Movie Analysis & Recommendation (IMDb Dataset)

Projet d’analyse de données et de machine learning appliqué à un jeu de données de films IMDB.  
L’objectif est d’explorer les facteurs influençant les notes des films et de proposer un système de recommandation basé sur la similarité des synopsis.

---

## Objectifs du projet

- Analyser statistiquement les notes IMDB de films
- Étudier l’influence des genres et des années de sortie
- Mettre en place un système de recommandation de films basé sur le contenu textuel (NLP)
- Illustrer une démarche complète de data analysis appliquée

---

## Concepts et compétences mobilisés

- Analyse exploratoire de données (EDA)
- Feature engineering (one-hot encoding des genres)
- Statistiques descriptives
- Visualisation de données
- Traitement du langage naturel (TF-IDF)
- Similarité cosinus
- Manipulation de données avec pandas

---

## Données

- Dataset de 1000 films IMDB
- Variables principales :
  - Année de sortie
  - Durée
  - Genres (multi-labels)
  - Note IMDB
  - Nombre de votes
  - Synopsis (Overview)

### Nettoyage effectué
- Suppression de variables incomplètes (Meta_score, Gross)
- Renommage des colonnes pour plus de clarté
- Transformation des genres en variables binaires

---

## Préparation et feature engineering

- Séparation des genres multiples en colonnes binaires (one-hot encoding)
- Nettoyage et normalisation des textes descriptifs
- Calcul de statistiques par genre
- Analyse temporelle des notes
- Lissage par moyenne glissante sur 5 ans

---

## Analyses réalisées

### Statistiques globales
- Note moyenne d’environ 7.95
- Faible variance, cohérente avec une sélection de films bien notés

### Analyse par genre
- Calcul de la note moyenne par genre
- Analyse du nombre de films par genre
- Visualisation de la répartition des genres

### Analyse temporelle
- Évolution de la note moyenne par année de sortie
- Utilisation d’une moyenne glissante pour identifier les tendances de fond

---

## Système de recommandation (NLP)

Un système simple de recommandation est basé sur les résumés des films.

### Méthode
- Vectorisation des synopsis avec TF-IDF
- Calcul de la similarité entre films via la similarité cosinus
- Recommandation des films les plus proches sémantiquement

### Exemple
Films similaires à *The Godfather* :
- Knives Out
- The Godfather: Part III
- Nebraska
- The Night of the Hunter

---

## Technologies utilisées

- Python
- pandas
- matplotlib
- scikit-learn
- Jupyter Notebook

---

## Lancer le projet

```bash
pip install pandas matplotlib scikit-learn
jupyter notebook
```
Puis lancer le notebook d'analyse

## Améliorations possibles
- Ajout de modèles prédictifs (régression sur la note IMDB)
- Intégration du nombre de votes comme variable explicative
- Utilisation d’embeddings plus avancés (Word2Vec, BERT)
- Création d’une interface utilisateur pour la recommandation

## Auteur
Pierre Duchesne
