# 🔢 Reconnaissance de chiffres manuscrits avec Computer Vision

Projet de Computer Vision utilisant un réseau de neurones convolutif (CNN) pour reconnaître automatiquement des chiffres écrits à la main.

## 🎯 Objectif

Développer un modèle d'IA capable de reconnaître avec une grande précision des chiffres manuscrits (0 à 9) à partir d'images, en s'appuyant sur le célèbre dataset MNIST (70 000 images).

## 🛠️ Technologies utilisées

- **Python 3**
- **TensorFlow / Keras** — Deep Learning
- **CNN (Convolutional Neural Network)** — architecture spécialisée pour les images
- **NumPy** — manipulation de matrices
- **Matplotlib** — visualisation

## 🧠 Architecture du modèle

| Couche | Rôle | Paramètres |
|--------|------|------------|
| Conv2D (32 filtres) | Détection de bords/formes basiques | 320 |
| MaxPooling | Réduction dimensionnelle | 0 |
| Conv2D (64 filtres) | Détection de patterns complexes | 18 496 |
| MaxPooling | Réduction dimensionnelle | 0 |
| Flatten | Aplatissement | 0 |
| Dense (64) | Combinaison de patterns | 102 464 |
| Dense (10) | Classification finale (softmax) | 650 |

**Total : 121 930 paramètres entraînables**

## 📊 Résultats

- **Précision sur l'entraînement : 99,03%**
- **Précision sur les données de test : 98,87%** ⭐
- Loss final : 0,0355

Sur 10 000 images jamais vues, le modèle reconnaît correctement 9 887 chiffres avec une confiance moyenne supérieure à 99%.

## 🔍 Démarche

1. Chargement et exploration du dataset MNIST
2. Normalisation des pixels (0-255 → 0-1)
3. Encodage des étiquettes (one-hot encoding)
4. Construction d'un CNN à 2 couches convolutives
5. Entraînement sur 5 epochs (batch size 128)
6. Évaluation sur les données de test
7. Visualisation des prédictions

## 💼 Applications business

Ce type de modèle peut être adapté à :
- Reconnaissance de documents scannés (factures, formulaires)
- Détection de produits défectueux sur ligne de production
- Comptage automatique sur images
- Reconnaissance de plaques d'immatriculation
- Lecture automatique de codes manuscrits

## 👤 Auteur

**Benjamin Gravé** — Data Analyst Freelance
📍 Belgique | 💼 [LinkedIn](https://www.linkedin.com/in/benjamin-gravé-217a0517)
