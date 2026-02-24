# 🧠 Pistachio Classification – Deep Learning Optimization Project

## 🚀 Overview

Ce projet présente une implémentation complète d’un pipeline de Deep Learning dédié à la classification automatique de pistaches à partir de caractéristiques numériques.

L’objectif est double :

* Construire un modèle MLP robuste pour la classification supervisée.
* Optimiser rigoureusement ses hyperparamètres via Optuna afin de maximiser la performance tout en contrôlant la généralisation.

Le projet adopte une approche méthodologique structurée : modélisation, régularisation, optimisation, évaluation statistique et analyse de robustesse.

---

## 🎯 Objectif

Développer un modèle de classification performant capable de :

* Maximiser la validation accuracy
* Minimiser le surapprentissage
* Maintenir une bonne capacité de généralisation
* Analyser finement les effets des hyperparamètres

---

## 📊 Dataset

Le dataset contient des caractéristiques numériques décrivant des pistaches.

Pipeline appliqué :

* Vérification des distributions
* Analyse des classes
* Normalisation des variables
* Split train / validation / test
* Encodage adapté aux labels

---

## 🏗️ Architecture du Modèle

Modèle : Multi-Layer Perceptron (MLP)

Architecture optimale trouvée :

* 3 couches cachées
* 64 → 96 → 128 neurones
* Activation : ReLU
* Batch Normalization
* Dropout ≈ 0.34
* Régularisation L2
* Optimizer : RMSprop
* Learning rate ≈ 0.00142

Validation Accuracy optimale : 96.22 %

---

## 🔬 Optimisation des Hyperparamètres

Méthode : Optuna (TPE Sampler)

Espace exploré :

* Nombre de couches
* Nombre de neurones par couche
* Dropout
* Learning rate
* Optimizer
* L2 regularization
* Weight decay
* Batch size

Durée d’optimisation : 26.42 minutes
Nombre de trials : exploratoire adaptatif

---

## 📈 Résultats

Le modèle final obtient :

* Validation Accuracy : 96.22 %
* Performance stable sur le test set
* Courbe ROC cohérente
* Matrice de confusion équilibrée
* Lift curve significative

Les analyses graphiques incluent :

* ROC Curve
* Confusion Matrix
* Lift Curve
* Impact du learning rate
* Impact du weight decay
* Distribution des prédictions
* Courbes d’apprentissage

---

## 🧠 Analyse & Interprétation

* Le modèle présente une excellente séparation des classes.
* La régularisation L2 + Dropout réduit efficacement l’overfitting.
* L’optimisation hyperparamétrique améliore significativement la robustesse.
* L’architecture progressive (64 → 96 → 128) favorise une extraction hiérarchique des représentations.

La stabilité des performances indique une bonne capacité de généralisation.

---

## 🛠️ Stack Technique

* Python
* TensorFlow / Keras
* Optuna
* NumPy / Pandas
* Matplotlib / Seaborn
* Kaggle GPU Environment

---

## 📦 Outputs Générés

* best_pistachio_model.h5
* Courbes ROC
* Matrices de confusion
* Lift curve
* Analyses d’impact hyperparamètres
* Visualisations d’optimisation

---

## 📌 Conclusion

Ce projet démontre l’importance :

* d’une architecture bien régularisée
* d’une optimisation hyperparamétrique méthodique
* d’une analyse statistique rigoureuse des performances

La combinaison modélisation + optimisation + interprétation constitue une approche complète et scientifiquement cohérente.

---

## 🔎 Perspectives

* Validation croisée K-fold
* Comparaison avec modèles CNN si données image
* SHAP / Feature importance
* Calibration probabiliste
* Ensemble learning

