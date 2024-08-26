---
layout: default
title: Concepts et technologies IA
---

<!-- Table of content -->
* TOC
{:toc}

# **Introduction**
Cette page présente les concepts et technologies de base utilisés en IA.
Pour chaque technologie, nous allons essayer de vous donner une explication poussée, des exemples d'utilisation, des ressources pour aller plus loin et ce qui se fait de mieux dans le domaine (parfois en doublon avec les infos présentes sur la page [Se mettre au développement](/pages/dev.md)).

# **Liens rapides**
- [Papers with code](https://paperswithcode.com/) Site référençant les articles de recherche en IA et les implémentations de ces articles. La section *Browse State-of-the-Art* permet de voir les modèles les plus performants pour chaque tâche (pas forcément les plus pratiques à utiliser). La section *Methods* fournit nottament les papiers de référence sur chaque sujet/technologie.
- Voir [Se mettre au développement](/pages/dev.md) pour des ressources sur comment trouver des jeux de données, des exemples de code, etc. 

# **Fondamentaux de Deep Learning**
Le **Deep Learning** est une branche de l'IA qui utilise des réseaux de neurones artificiels (au sens large) pour apprendre à partir de données. Cette section présente les concepts de base du Deep Learning, qui sont utilisés dans la plupart des applications d'IA modernes (classification d'images, traitement du langage naturel, reconnaissance vocale, reinforcement learning, etc.).

## **[MLP (Multi-Layer Perceptron)](#mlp-multi-layer-perceptron)**
Le MLP (Multi-Layer Perceptron) est un type de réseau de neurones composés de plusieurs couches de neurones. Chaque couche de neurones est connectée à la couche précédente et à la couche suivante. Les MLP sont utilisés pour résoudre des problèmes de classification et de régression. Ce concept est l'ancêtre des réseaux de neurones modernes (CNN, RNN, etc.). IL reste cependant très utilisés pour des problèmes simples et même tel quel dans certaines architectures complexes (GAN, etc.).

Il permet également de se familiariser avec de nombreux concepts de base comme les fonctions d'activation, de coût, la descente de gradient, etc.

### Explications
- [3Blue1Brown](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi) Vidéos 1 à 4, bonne explications des mathématiques sous-jacentes, même si elle est un peu lente. Il peut être intéressant d'essayer d'implémenter un MLP à la main à partir de ces vidéos uniquement pour bien comprendre le fonctionnement.

### Technologies
- [TensorFlow](https://www.tensorflow.org/guide/keras/sequential_model) Implémentation de MLP avec TensorFlow.
- [PyTorch](https://pytorch.org/tutorials/beginner/blitz/neural_networks_tutorial.html) Présentation des réseaux de neurones (dont MLP) avec PyTorch. Les *nn.Linear* sont les couches de neurones, les *nn.Conv2d* sont les couches de convolutions voir [CNN](#cnn-convolutional-neural-network).

## **[CNN (Convolutional Neural Network)](#cnn-convolutional-neural-network)**
Les CNN (Convolutional Neural Networks) sont un type de réseau de neurones utilisés pour traiter des données structurées en grille, nottament des images. Les CNN sont composés de plusieurs couches de neurones, dont des couches de convolution, des couches de pooling et des couches entièrement connectées (MLP). Les CNN sont utilisés pour résoudre des problèmes de classification d'images, de détection d'objets, de segmentation d'images, etc.

### Explications
Pour comprendre ce qu'est un filtre, et ce à quoi ils peuvent servir:
- [Image Kernels Explained](https://setosa.io/ev/image-kernels/) Explication des filtres et de leur utilisation.
- [Convolutional Neural Networks (CNNs) explained](https://ujjwalkarn.me/2016/08/11/intuitive-explanation-convnets/) Très bonne explication des CNN. Cependant, les maths ne sont pas vraiment abordées. De plus, cet article date un peu (2016), et les architectures de CNN ont évoluées depuis. Certains liens ne fonctionnent également plus. Les architectures les plus récentes sont décrites dans la section suivante.
- [Mathématiques et implémentation](https://www.youtube.com/watch?v=Lakz2MoHy6o) Explication des mathématiques derrière les CNN et implémentation à la main (pur numpy).

### Technologies
- [TensorFlow](https://www.tensorflow.org/tutorials/images/cnn) Exemple d'utilisation de CNN avec TensorFlow.
- [PyTorch](https://pytorch.org/tutorials/beginner/blitz/cifar10_tutorial.html) Exemple d'utilisation de CNN avec PyTorch.

De manière générale, il est plus simple d'utiliser des **modèles pré-entrainés** et de les adapter à votre problème. Cela permet de gagner du temps et d'obtenir de (bien) meilleures performances.

- Pour la **classification d'images**, parmis les modèles préentrainés les plus populaires, on peut citer:
  - **ResNet**: Famille de modèle la plus populaire, ses modèles sont très profonds (beaucoup de couches). Les modèles les plus populaires sont ResNet-50 et ResNet-101.
  - **EfficientNet**: Famille de modèle très récente, ils sont très performants et très légers : c'est le meilleur moyen d'atteindre de très bonnes performances rapidement. Ils vont de B0 (le plus léger) à B7 (le plus lourd).
  - Mais aussi: **VGG**, **Inception**, **DenseNet** sont des alternatives à ResNet très populaires, **MobileNet** très léger, est utilisé pour des applications mobiles, ...
  - De manière générale, **n'importe lequel de ces modèles** peut être utilisé pour de la classification d'images. Cependant, pour des tâches plus spécifiques (détection d'objets, segmentation, etc.) ou en fonction de contraintes de performances, certains modèles seront plus adaptés que d'autres.
- Pour la **détéction d'objet**, on peut citer:
  - **YOLO** : Famille de modèle très populaire pour la détection d'objets en temps réel. Il est probablement le plus utilisé et donc le mieux documenté. Il donne de très bons résultats pour la plupart des cas d'utilisation, même en temps réel.
  - **Faster R-CNN** : Modèle (pas mal) plus lourd que YOLO, mais plus précis. Il est utilisé pour des applications où la précision est plus importante que la vitesse. Il est également plus performant pour des entraînements sur des jeux de données plus petits. Il est bien plus efficace que les autres modèles présentés pour les objets de petite taille.
  - **EfficientDet** : Modèle très récent, très performant et très léger (plus rapide que YOLO). Il est une excellente alternative aux deux modèles précédents.
  - **RetinaNet** : Modèle très performant pour la détection d'objets, il est très utilisé pour des applications où la précision est importante.

La plupart de ces modèles sont disponibles sur:
  - [TensorFlow Hub](https://tfhub.dev/s?module-type=image-feature-vector&tf-version=tf2) Modèles pré-entrainés pour TensorFlow.
  - [PyTorch Hub](https://pytorch.org/hub/) Modèles pré-entrainés pour PyTorch.

## **[Transformer](#transformer)**
Les Transformers sont une architecture utilisée pour traiter des **données séquentielles,** comme du texte ou de la parole. Les Transformers sont composés de plusieurs couches d'attention, de couches de feedforward (voir [MLP](#mlp-multi-layer-perceptron)) et de couches de normalisation. Les Transformers et le principe d'attention ont révolutionné le traitement du langage naturel et ont permis de réaliser des avancées significatives dans des tâches telles que la traduction automatique, la génération de texte, la classification d'images, etc.. Ils sont à la base des LLM (GPT-4, Gemini, ...)
Les transformers sont plus compliqués à comprendre que les CNN ou les MLP, mais ils sont très puissants et très flexibles.

> Publié en 2017, le modèle Transformer a été introduit dans l'article [Attention is all you need](https://arxiv.org/abs/1706.03762) (View PDF sur la droite) par Vaswani et al. Ce papier, avec plus de 130 000 citations (4e plus cité de tous les temps), est probablement le plus influent de ces dernières années.

### Explications
Pour comprendre la motivation derrière les Transformers, il faudrait présenter les RNN (Recurrent Neural Networks) et les LSTM (Long Short-Term Memory), mais ces modèles sont devenus (quasiment) obsolètes depuis l'arrivée des Transformers. Les RNN et LSTM sont des modèles qui traitent les données séquentiellement, ce qui les rend très lents et peu performants. Les Transformers, en revanche, **traitent les données de manière parallèle** (mécanisme d'attention), ce qui les rend beaucoup plus rapides et plus performants, nottament grâce à la parrallélisation des calculs sur GPU.

### Technologies
Les Transformers sont surtout utilisés dans des architectures plus complexes, comme les GPT (Generative Pre-trained Transformer) ou les ViT (Vision Transformer). Il est donc plus pertinent de les découvrir à travers ces modèles et ces applications (voir [LLM](#llm-large-language-models)). Cependant, si vous voulez comprendre les Transformers de manière plus générale, voici quelques ressources:
- [3Blue1Brown](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi) Vidéos 5 et 6, explication visuelle et intuitive des transformers et du mécanisme d'attention à travers l'exemple de la prédiction de texte ([LLM](#llm-large-language-models)).
- [The Illustrated Transformer](http://jalammar.github.io/illustrated-transformer/) Très bonne explication des Transformers, illustrée et basée sur le papier original. Cependant, elle reste chargée en informations et peut être difficile à suivre.

Pour ce qui est des implémentations, PyTorch et TensorFlow proposent des implémentations de Transformers prêtes à l'emploi:
- [PyTorch](https://pytorch.org/docs/stable/generated/torch.nn.Transformer.html) Documentation: implémentation officielle des transformers pour PyTorch. Prête à l'emploi et simple à utiliser.
- [Tarx](https://github.com/google/trax) Bibliothèsque officielle des Transformers pour TensorFlow.
- [TensorFlow](https://www.tensorflow.org/tutorials/text/transformer) (Très bon) Tutoriel d'implémentation de Transformers avec TensorFlow.

# **Applications de Deep Learning**

## **[LLM (Large Language Models)](#llm-large-language-models)**

Les LLM (Large Language Models) sont un terme générique pour désigner des modèles de traitement du langage naturel (souvent basés sur des architectures neuronales) qui sont entraînés sur de très grands jeux de données. Ainsi, ils peuvent désigner à la fois des modèles génératifs comme ChatGPT, Gemini ou leur modèles sous-jacents de prédiction de texte mais aussi des modèles de classification de texte ou autre. Aujourd'hui, **le mot LLM tend à désigner les assistants virtuels** (ChatGPT, Gemini, Claude, ...).
Tous ces assistants sont basés sur des modèles de prédiction de texte (à partir d'une suite de mot, quel est le prochain mot le plus probable ?), qui sont ensuite légerement réentrainés sur des données plus spécifiques (moralement des exemples de conversation entre agent virtuel et humain). Malhereusement, ces modèles sous-jacents diffèrent d'un assistant à l'autre (bien qu'ils utilisent tous des transformers ou dérivés). Pour mieux comprendre ces modèles de prédiction de texte, on va se concentrer sur **les modèles GPT (Generative Pre-trained Transformer)**, à la base de ChatGPT.

### Explications
Les explications les plus exhaustives sur les LLM sont souvent données dans les articles de recherche qui les décrivent ([GPT-2](https://d4mucfpksywv.cloudfront.net/better-language-models/language-models.pdf), [GPT-3](https://arxiv.org/pdf/2005.14165v4)). Cependant, ces articles sont souvent très techniques et peu accessibles pour les débutants (*PS: le code source de GPT-3 et GPT-4 est privé*). Les vidéos de [3blue1brown](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi) sont une bonne introduction. 

Pour aller plus loin, la chaîne youtube de **Andrej Karpathy** (cofondateur de OpenAI, ex-directeur de l'IA de Tesla) est une mine d'or pour comprendre l'implémentation des LLM. Dans une série de 3 vidéos (10 heures quand même), il reconstruit nottament entièrement GPT-2 à partir de zéro, en expliquant chaque étape et chaque choix de conception.
- [Partie 1](https://www.youtube.com/watch?v=kCc8FmEb1nY) (*1h56*) : Version naïve d'un GPT. Réalisation d'un modèle prédisant du texte cohérent.
- [Partie 2](https://www.youtube.com/watch?v=SGZ6BttHMPw) (*2:13*) : Présentation d'un tokenizer, cette vidéo est intéréssante, mais n'est pas nécéssaire et peut être sautée.
- [Partie 3](https://www.youtube.com/watch?v=3MqJzMvHE3E) (*4:01*) : Réalisation d'un modèle de prédiction de texte avec des performances proches de GPT-2.

Il a également réalisé une [**conférence**](https://www.youtube.com/watch?v=zjkBMFhNj_g) d'une heure se focalisant sur les LLM. Il y présente à la fois la réalité des modèles actuels, des ordres de grandeurs (temps, argent), les limites actuelles et les perspectives d'avenir. **C'est un tour d'horizon très complet de la situation actuelle des LLM**, et elle peut être écoutée en audio uniquement pour les plus pressés. Le visionnage des 3 vidéos précédentes n'est pas nécéssaire.

[Back to Home](../index.md)
