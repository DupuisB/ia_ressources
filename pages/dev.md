---
layout: default
title: Se mettre au développement
---

<!-- Table of content -->
* TOC
{:toc}

# **Introduction**

Se lancer dans le domaine de l'IA peut sembler intimidant. La complexité des approches actuelles (qui ne le sont pas tant que ca pour la plupart) peuvent donner l'illusion que le moindre projet est compliqué. Et même sans cette impression, il semble, au vu des TIPEs de certains de nos camarades, qu'il faut consacrer à minima quelques dixaines d'heures avant de pouvoir bien apréhender les premiers concepts. En réalité, **pour tous les élèves de Télécom,** qui ne sont plus complétement novice en mathématiques et en informatique, **il est possible de comprendre et de réaliser ses premiers modèles (par exemple de reconnaissance d'image) en seulement quelques heures sans connaissances préalables.**

# **[Son premier projet: MLP et CNN](#son-premier-projet)**

Pour commencer le deep learning, il semble important de se familiariser en premier avec les concepts de [MLP](/pages/concepts.md#mlp), puis de [CNN](/pages/concepts.md#cnn).

Commencons par le [MLP](/pages/concepts.md). Voici une proposition pour commencer :  

Ici, on se basera sur les vidéos 1 à 4 de [cette playlist]([3Blue1Brown](https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi)) de 3blue1brown.  

Commencer par **regarder les vidéos 1, 2 et 3** (en accélérée si vous voulez, elles ne sont pas très denses). Elles introduisent les concepts de neurone artificiel, de fonction d'activation, de rétropropagation, etc. Ses concepts sont essentiels pour comprendre le fonctionnement des réseaux de neurones. La 4ème vidéo explique les mathématiques et l'implémentation de la rétropropagation. Elle est plus optionnelle, mais reste importante et surtout pas très compliquée (c'est un (tout petit) peu de calcul diff.).  

A partir de là, vous pouvez commencer à coder votre premier réseau de neurones. Pour cela, deux options s'offrent à vous :  

- A partir de la **vidéo 4** et seuelement cette ressource, vous pouvez essayer **d'implémenter votre propre réseau en python (avec numpy uniquement)**. Cela peut être un peu fastidieux (il faut se poser avec une feuille et ne pas avoir peur d'écrire les équations), mais c'est un très bon exercice pour bien assimiler certains concepts de bases, qui se retrouvent partout en deep learning. Pour le tester, vous pouvez utiliser le dataset [Fashion MNIST](https://github.com/zalandoresearch/fashion-mnist), très similaire au MNIST utilisé dans la vidéo.

- Sinon, ou si vous avez fini la précédente, **vous pouvez suivre les tutoriels de [PyTorch](https://pytorch.org/tutorials/beginner/blitz/neural_networks_tutorial.html) ou de [Tensorflow](https://www.tensorflow.org/tutorials/quickstart/beginner) pour implémenter un réseau de neurones.** (voir [Quel est la différence entre PyTorch et Tensorflow ?](#pytorch-vs-tensorflow)). A partir de là, vous pouvez aussi utiliser le dataset [Fashion MNIST](https://github.com/zalandoresearch/fashion-mnist) pour essayer votre implémentation. Si vous utilisez PyTorch et galérez, voici un [exemple](https://www.kaggle.com/code/mishra1993/pytorch-multi-layer-perceptron-mnist).

> Notez que pour ces deux approches, un ordinateur sans GPU donne des performances très correctes pour des réseaux de petite taille. **Réaliser ce premier projet sur un ordinateur personnel est donc tout à fait possible** (et même recommandé pour apprendre à installer les librairies, etc.)

Une fois votre premier réseau MLP crée à l'aide d'un framework de deep learning, **vous pouvez essayer d'implémenter un [CNN](/pages/concepts.md#cnn)**, pour le même problème. Les bibliotheques traitant un MLP et un CNN de la même manière, cela devrait être (relativement) rapide.

# **Présentation de Kaggle**

Kaggle est une plateforme de **compétitions en data science et en machine learning**. Rachété par Google en 2017, c'est aujourd'hui l'une des meilleures ressources pour se mettre au machine learning. Le site est **entièrement gratuit, mais demande une inscription** (compte Google). 
Son essence est de proposer des compétitions, souvent sponsorisé par des organisations.

![Page accueil Kaggle](/assets/images/kaggle_accueil.png)

Certains, catégorisés `knowledge` sont des compétitions d'entrainement, ou chacun peut participer et proposer sa solution et de la comparer à celles des autres. L'une des grandes forces de Kaggle est, une fois une compétition choisie, la partie `Code` permet de voir le code et la solution de l'ensemble des autres participants. Cela permet de voir comment les autres ont résolu le problème, surtout que beaucoup de participants sont des professionnels qui veillent à faire des solutions claires et bien commentées, souvent sous forme de tutoriels.

![Page code Kaggle](/assets/images/kaggle_code.png)

> Notez que Kaggle repose sur l'usage extensif et exclusif de **Notebooks Jupyter fonctionnants sous Python** (ou R). Cela est très utilisé et souvent bien pratique, mais est très limité pour des projets plus conséquents. Toutes les compétitions acceptent des solutions aux données de test sous forme d'un simple fichier de données (en général un fichier csv ou json), mais il est souvent plus simple de proposer une solution sous forme de notebook (qui peut être exécuté directement sur la plateforme).

Aujourd'hui, Kaggle est un peu plus que cela. Le site propose des **cours en ligne** (gratuits et très qualitatifs) sur des sujets de data science et de machine learning. Il propose également des **datasets** (voir [Où trouver des jeux de données ?](#dataset)) et des **Modèles pré-entrainés** faciles à télécharger et/ou à utiliser (Pour le traitement du language natural (NLP), on lui préferera [HuggingFace](https://huggingface.co/), mais kaggle dispose des principaux modèles).

# **Ressources utiles**

## **[Où trouver des jeux de données ?](#dataset)**

- **[Kaggle](https://www.kaggle.com/datasets)** : énorme base de données (inscription gratuite requise), probablement la plus diverse existante. Il est possible de trouver des données sur à peu près n'importe quel sujet, de taille et de qualité très variable : certains filtres permettent de limiter à des datasets de qualités. On regrette le faible nombre de filtres, rendant difficile le tri par langue ou par sujet.

- **[Google Dataset Search](https://datasetsearch.research.google.com/)** : moteur de recherche de datasets, permet de trouver des datasets sur n'importe quel sujet. Les résultats sont des liens vers des sites externes, il est donc possible de trouver des datasets sur Kaggle, mais aussi sur des sites gouvernementaux, des universités, etc. A l'aide des bons mots clés, c'est la solution la plus puissante, mais pas forcément la plus pratique: cela peut prendre beaucoup de temps pour trouver un jeu de donnée précis. Vous pouvez le voir comme un équivalent de google scholar pour les datasets. **Le moteur classique de Google** peut également donner de très bons résultats.

- **[HuggingFace](https://huggingface.co/datasets)** : Un large choix de datasets crées pour des taches de machine learning. Ils ont l'avantage de pouvoir être importé en une seule ligne de code python grâce à [leur bibliothèque](https://github.com/huggingface/datasets).

- **[data.gouv.fr](https://www.data.gouv.fr/)** : site officiel du gouvernement pour l'open data francaise. Il regroupe les catalogues des différents ministères et d'un grand nombre de communes, villes, départements, régions. A cela s'ajoutent les datasets de plusieurs organismes, comme OpenStreetMap ou l'INSEE. Cependant, il ne semble pas y avoir tous les datasets de ces organisations, et il est parfois nécéssaire d'aller sur les sites des differents organisme (par exemple en tapant `open data département savoie`).

## **[Bibliothèques utiles](#bibliotheques-utiles)**

A peu près toutes les bibliothèques dont vous pouvez avoir besoin sont trouvables sur **[Best of ML](https://github.com/ml-tooling/best-of-ml-python)**. Cependant, ce document est un peu long et les bibliothèques avec le plus de stars ne sont pas forcément les plus adaptées ni les plus utilisés. Voici une liste (plus courte) des bibliothèques les plus pertinentes :

- **PyTorch** et **TensorFlow** : les deux librairies les plus utilisées en deep learning. Voir [Quel est la différence entre PyTorch et TensorFlow ?](#pytorch-vs-tensorflow) pour plus d'informations.

### **Pour l'analyse et le traitement de données**

- **Pandas** : librairie de manipulation de données en python, très utilisée en data science. Elle permet de manipuler des données tabulaires de manière très efficace.

- **Matplotlib** et **Seaborn** : librairies de visualisation de données en python. Matplotlib est la librairie de visualisation de données la plus utilisée en python, mais elle est souvent jugée peu pratique. Seaborn est une surcouche de Matplotlib, qui permet de faire des graphiques plus facilement.

- **Scikit-learn** : librairie de machine learning en python, très utilisée en data science. Elle permet de réaliser des tâches de machine learning de manière très simple.

### **Pour le traitement d'image**

- **OpenCV** : librairie de computer vision. Elle permet de réaliser des tâches de détection d'objet, de segmentation d'image, de tracking, etc. mais aussi des tâches plus simples (redimensionner une image, changer ses metadonnées, etc.). Elle est très utilisée mais peut être bien trop compliquée à installer et utiliser pour des tâches simples.

- **Pillow** : librairie de traitement d'image en python, plus simple que OpenCV. Elle est souvent utilisée pour des tâches de traitement d'image plus simples (redimensionner une image, changer ses metadonnées, ses couleurs, etc.). Elle est très simple à installer et à utiliser.

### **Pour le reinforcement learning**

- **[Gymnasium](https://github.com/Farama-Foundation/Gymnasium)** : le successeur officiel de OpenAI Gym, qui est une librairie de reinforcement learning en python. Elle permet de créer des environnements de reinforcement learning (i.e. des interfaces entre les algorithmes de reinforcement learning et les environnements (jeux, ...)). Voir **PettingZoo** pour une version multi-agent.

- **[PettingZoo](https://github.com/Farama-Foundation/PettingZoo)** : version multi-agent de Gymnasium, qui permet de créer des environnements de reinforcement learning multi-agent.

- **[CleanRL](https://github.com/vwxyzjn/cleanrl)** : quelques dixaines d'exemples d'algoritme de reinforcement learning en python. Tous les exemples sont constitués d'un unique fichier. Elle permet de partir d'une base de qualité pour l'adapter à ses besoins.

# **Questions diverses**

## **[Quel est la différence entre PyTorch et Tensorflow ?](#pytorch-vs-tensorflow)**
PyTorch et TensorFlow sont de loin les 2 librairies les plus utilisées en deep learning, chacune largement documentée et utilisée. Notez que certains y ajoutent [Keras](#keras), qui est une surcouche de TensorFlow.  

Bien que les deux librairies permettent de réaliser les mêmes tâches (à peu près n'importe quel projet de deep learning peut être réalisé avec l'une ou l'autre), elles ont des différences qui peuvent rendre l'une ou l'autre plus adaptée à un projet donné. Si vous voulez une comparaison technique détaillée, allez sur internet, mais ce qu'il faut noter est qu'elles ne s'addressent pas au même public :

- **PyTorch** est plus simple à prendre en main, et est souvent préféré pour les projets de recherche, où l'on veut tester rapidement des idées. Il est plus flexible, et permet de faire des choses plus "sales" (comme modifier les poids d'un réseau de neurones à la main). De manière générale, elle est plus adaptée pour apprendre et découvrir le deep learning, même à un niveau très avancé (la plupart des chercheurs l'utilisent). C'est notre recommandation pour débuter.

> **OpenAI** (précedemment sous TensorFlow), **Meta** (développeurs de PyTorch),**Apple**, **AMD**, **Microsoft**, ...  utilisent PyTorch comme framework principal pour entraîner leur modèles. A noter qu'elles utilisent souvent TensorFlow pour d'autres applications.

- **TensorFlow** est largement utilisé en production et est souvent choisi pour les projets où des performances optimales sont cruciales, grâce à son approche d'exécution déclarative (que je ne détaillerai pas ici, imaginez la différence entre compilé et interprété, en plus petit), même si cela peut rendre le débogage un peu moins simple. Son autre grande force réside dans sa capacité à être déployé à grande échelle. Pour les développeurs, c'est actuellement le framework le plus demandé. Sa courbe d'apprentissage est plus raide, et il peut être difficile de commencer, mais l'intégration du module [Keras](#keras) a simplifie grandement les choses.

> **Google** (les développeurs, qui commencent à utiliser [JAX](https://github.com/google/jax)), **Tik Tok**, **Wallmart**, **PwC**, **JPMorgan**, ... utilisent TensorFlow comme framework principal pour entraîner leur modèles. A noter qu'elles utilisent souvent PyTorch pour d'autres applications.

## **[Qu'est-ce que Keras ?](#keras)**

**Keras**, dévéloppé par Françoit Chollet (de l'ENSTA, travaille chez Google), est un **framework de haut niveau** pour le deep learning. Principalement intégré à TensorFlow, il fonctionne maintenant avec PyTorch et Jax (et CND). **Son nieau d'abstraction est plus élevé que PyTorch ou TensorFlow**, il est alors encore plus simple d'implémenter certains modèles. Une fois ce modèle implémenté, il est alors possible de choisir le framework sous-jacent en fonction de ses besoins (même si il reste légerement moins efficace que du natif pour chacun d'entre eux). Cette abstraction vient au cout d'une perte de contrôle sur bas niveau (qui peut être contourné en melangeant keras et TensorFlow). **Pour un développement rapide, c'est très efficace.**   

> **Netflix**, **Uber** utilisent intensivement keras. La plupart des autres entreprises mentionnées l'utilisent dans une certaine mesure.

[Back to Home](../index.md)
