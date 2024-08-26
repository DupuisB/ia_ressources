---
layout: default
title: Concepts et technologies IA
---

<!-- Table of content -->
* TOC
{:toc}

# Introduction
Pour chaque technologie, nous allons essayer de vous donner une explication poussée, des exemples d'utilisation, des ressources pour aller plus loin et ce qui se fait de mieux dans le domaine.

# Vocabulaire
### IA
L'intelligence artificielle (IA) est un domaine de l'informatique qui consiste à créer des programmes informatiques capables de réaliser des tâches typiquement humaines, comme la reconnaissance de la parole, la prise de décision, la traduction de langues, etc.

### Machine Learning
Le machine learning est une branche de l'intelligence artificielle qui consiste à créer des programmes informatiques capables d'apprendre à partir de données. Ces programmes sont capables de s'améliorer au fur et à mesure qu'ils sont exposés à de nouvelles données.

### Deep Learning
Le deep learning est une branche du machine learning qui consiste à créer des réseaux de neurones artificiels capables d'apprendre à partir de données. Ces réseaux de neurones sont capables de s'auto-organiser et de s'auto-optimiser pour résoudre des problèmes complexes.

# **Concepts**

## **[MLP (Multi-Layer Perceptron)](#mlp-multi-layer-perceptron)**
Le MLP (Multi-Layer Perceptron) est un type de réseau de neurones composés de plusieurs couches de neurones. Chaque couche de neurones est connectée à la couche précédente et à la couche suivante. Les MLP sont utilisés pour résoudre des problèmes de classification et de régression. Ce concept est l'ancêtre des réseaux de neurones modernes (CNN, RNN, etc.). IL reste cependant très utilisés pour des problèmes simples et même tel quel dans certaines architectures complexes (GAN, etc.).

Il permet également de se familiariser avec de nombreux concepts de base comme les fonctions d'activation, de coût, la descente de gradient, etc.

### Explications
- [3Blue1Brown](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi) Vidéos 1 à 4, bonne explications des mathématiques sous-jacentes, même si elle est un peu lente. Il peut être intéressant d'essayer d'implémenter un MLP à la main à partir de ces vidéos uniquement pour bien comprendre le fonctionnement.

### Technologies
- [TensorFlow](https://www.tensorflow.org/guide/keras/sequential_model) Implémentation de MLP avec TensorFlow.
- [PyTorch](https://pytorch.org/tutorials/beginner/blitz/neural_networks_tutorial.html) Présentation des réseaux de neurones (dont MLP) avec PyTorch. Les *nn.Linear* sont les couches de neurones, les *nn.Conv2d* sont les couches de convolutions voir [CNN](#cnn-convolutional-neural-network).

### Exemples
- [Kaggle](https://www.kaggle.com/c/digit-recognizer) Compétition Kaggle sur la reconnaissance de chiffres manuscrits.


## **[CNN (Convolutional Neural Network)](#cnn-convolutional-neural-network)**
Les CNN (Convolutional Neural Networks) sont un type de réseau de neurones utilisés pour traiter des données structurées en grille, nottament des images. Les CNN sont composés de plusieurs couches de neurones, dont des couches de convolution, des couches de pooling et des couches entièrement connectées (MLP). Les CNN sont utilisés pour résoudre des problèmes de détection d'objets, de segmentation d'images, etc.

### Explications
Pour comprendre ce qu'est un filtre, et ce à quoi ils peuvent servir:
- [Image Kernels Explained](https://setosa.io/ev/image-kernels/) Explication des filtres et de leur utilisation.
- [Convolutional Neural Networks (CNNs) explained](https://ujjwalkarn.me/2016/08/11/intuitive-explanation-convnets/) Très bonne explication des CNN. Cependant, les maths ne sont pas vraiment abordées. De plus, cet article date un peu (2016), et les architectures de CNN ont évoluées depuis. Certains liens ne fonctionnent également plus. Les architectures les plus récentes sont décrites dans la section suivante.
- [Mathématiques et implémentation](https://www.youtube.com/watch?v=Lakz2MoHy6o) Explication des mathématiques derrière les CNN et implémentation à la main (pur numpy).

### Technologies
- [TensorFlow](https://www.tensorflow.org/tutorials/images/cnn) Exemple d'utilisation de CNN avec TensorFlow.
- [PyTorch](https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html) Exemple d'utilisation de CNN avec PyTorch.
> De manière générale, il est plus simple d'utiliser des modèles pré-entrainés pour des problèmes de classification d'images et de les adapter à votre problème. Cela permet de gagner du temps et d'obtenir de (bien) meilleures performances.
- Parmis les modèles préentrainés les plus populaires, on peut citer:
  - **ResNet**: Famille de modèle la plus populaire, ses modèles sont très profonds (beaucoup de couches). Les modèles les plus populaires sont ResNet-50 et ResNet-101.
  - **EfficientNet**: Famille de modèle très récente, ils sont très performants et très légers : c'est le meilleur moyen d'atteindre de très bonnes performances rapidement. Ils vont de B0 (le plus léger) à B7 (le plus lourd).
  - Mais aussi: **VGG**, **Inception**, **DenseNet** sont des alternatives à ResNet très populaires, **MobileNet** très léger, est utilisé pour des applications mobiles, ...
  - De manière générale, **n'importe lequel de ces modèles** peut être utilisé pour de la classification d'images. Cependant, pour des tâches plus spécifiques (détection d'objets, segmentation, etc.) ou en fonction de contraintes de performances, certains modèles seront plus adaptés que d'autres.

La plupart de ces modèles sont disponibles sur:
  - [TensorFlow Hub](https://tfhub.dev/s?module-type=image-feature-vector&tf-version=tf2) Modèles pré-entrainés pour TensorFlow.
  - [PyTorch Hub](https://pytorch.org/hub/) Modèles pré-entrainés pour PyTorch.

[Back to Home](../index.md)
