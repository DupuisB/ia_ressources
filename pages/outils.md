---
layout: default
title: Meilleurs outils IA
---

<!-- Table of content -->
* TOC
{:toc}

# Chatbots

## En ligne
[:star: ChatGPT](https://chatgpt.com/) - Chatbot de OpenAI
[:star: Claude](https://claude.ai/) - Chatbot d'Antropic
[:star: Groq](https://groq.com/) - Chatbot très rapide / Modèles LLaMA 3.1, Gemma et Mixtral disponibles
[:star: SciSpace](https://typeset.io/) - Trouver des papiers de recherche pour répondre à une question. [:star: Consensus](https://consensus.app/) est une alternative.

## En local
[:star: Jan](https://jan.ai/) - Solution complète et simple pour télécharger et utiliser des chatbots en local. Beaucoup plus rapide si vous avez un GPU Nvidia / une puce Apple série M.
[:star: llama.cpp](https://github.com/ggerganov/llama.cpp) - Bibliothèque C++ spécialisée dans l'inférence de modèles open source (nottament LLaMA). Il peut également être utilisé sous [Python](https://github.com/abetlen/llama-cpp-python), [Go](https://github.com/go-skynet/go-llama.cpp) et tout les languages principaux.

## Pour coder
[:star: EvalPlus](https://evalplus.github.io/leaderboard.html) - Leaderboard des différents LLMs sur des taches de code. Copilot est basé sur GPT 4o (pas encore évalué, mais surement proche de GPT 4 Turbo, ancienne base).
[:star: Github Copilot](https://github.com/features/copilot) - Assistant de code de Github, intégré à VSCode, IntelliJ, ... Gratuit pour les [étudiants](https://education.github.com/pack). / Complétion de code et chat.
[:star: Codeium](https://codeium.com/) - Alternative à Github Copilot, tout aussi bien supporté par les IDEs, mais gratuit.

# Génération d'images

## En ligne

[Microsoft Designer](https://designer.microsoft.com/image-creator) - Dalle-3 gratuitement (modèle de GPT-4). Gratuit mais assez lent. Très censuré (impossible de générer des images de personnalités par exemple).
[Ideogram](https://ideogram.ai/) - Très bon modèle (comparable à Midjourney 6). Environ 20 images gratuites par jour.
[Fastflux](https://fastflux.ai/) - Modèle très rapide, sans inscription. Qualité bien moindre, mais le plus rapide (1 seconde max)

## En local

La génération d'image en local requiert : un modèle (ses poids et son architecture) et un environnement d'exécution (bibliothèques pour réaliser l'inférence efficacement). Pour faciliter et automatiser ce processus, il est commun d'utiliser une interface pour télécharger et utiliser ces modèles. Voici quelques recommendations :

[:star: Stability Matrix](https://lykos.ai/) - Permet de télécharger des interfaces et des modèles. Rend facile le changement d'interface.
[Stable diffusion Webui](https://github.com/AUTOMATIC1111/stable-diffusion-webui) - De loin la plus utilisée (33e repo avec le plus de stars).
[DiffusionBee](https://github.com/divamgupta/diffusionbee-stable-diffusion-ui) - Interface minimaliste pour mac.
[ComfyUI](https://github.com/comfyanonymous/ComfyUI) - Interface de type graph. Permet de réaliser des chaines d'actions (workflow) complexes et complètes.

# Génération vidéo

Les IA génératives de vidéo n'en sont encore qu'à leurs débuts (les premiers papiers présentant des modèles "performants" datent de milieu - fin 2023). **On peut s'attendre à des progrès rapides dans les prochains mois et années.**
A la rentrée 2024, le meilleur modèle reste **Sora**, un modèle privé développé par OpenAI. Actuellement, les solutions publiques semblent essayer de rattraper leur retard.

[:star: Pixverse](https://pixverse.ai/) - Génération vidéo. Crédits gratuits chaque jour.
[:star: Dream Machine](https://lumalabs.ai/) - Génération vidéo. 30 générations gratuites par mois.
[:star: Runway](https://app.runwayml.com/) - Génération vidéo. Meilleur outil disponible. Quelques crédits gratuits, mais sont difficiles à utiliser.


# Divers

[:star: FMHY](https://fmhy.pages.dev/ai) - Collection plus grande d'outils. Attention, certains peuvent être illégaux (pas trop dans la page IA, surtout sur le reste du site). La plupart des sites présents ici peuvent être retrouvé là bas.

[Back to Home](../index.md)