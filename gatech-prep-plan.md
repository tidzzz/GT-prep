# Plan de préparation Georgia Tech — ML & Math

> 19 semaines | 20 avril 2026 → 24 août 2026
> Rentrée GT : 25 août 2026 | Fin de stage : 27 juillet 2026

---

## Comment utiliser ce document

- Je coche chaque item au fur et à mesure : `[ ]` → `[x]`
- Chaque dimanche : j'écris 2-3 lignes dans la section **Journal** en bas de la semaine (ce qui a marché, ce qui a bloqué, ce que je dois retravailler)
- Règle d'or : **jamais une ligne de code ML sans pouvoir expliquer à voix haute ce qu'elle fait**
- Deux tracks :
  - **Core** (non-négociable, ~8h/semaine)
  - **Bonus** (modulable, accélérateur quand j'ai du temps)

---

## Setup initial — semaine du 16 avril

- [ ] Souscrire à **Colab Pro** (~10 USD/mois)
- [ ] Créer un compte **Kaggle** (GPU T4 gratuit, 30h/semaine — backup)
- [ ] Installer **Anki** + créer un deck `ML-Math` pour les formules et concepts clés
- [ ] Créer le repo GitHub **`gatech-prep`** (public) avec README qui liste les phases
- [ ] Setup Obsidian (ou Notion) pour les notes perso
- [ ] Télécharger/localiser les PDFs :
  - [ ] Mathematics for Machine Learning (Deisenroth, Faisal, Ong) — https://mml-book.github.io
  - [ ] Pattern Recognition and Machine Learning (Bishop)
  - [ ] Probabilistic Machine Learning (Murphy)
  - [ ] Deep Learning (Goodfellow)
  - [ ] Convex Optimization (Boyd & Vandenberghe) — https://web.stanford.edu/~boyd/cvxbook/
  - [ ] Elements of Information Theory (Cover & Thomas)
  - [ ] Reinforcement Learning (Sutton & Barto)
- [ ] Bookmarker les cours :
  - [ ] CS229 Stanford (notes + vidéos 2018) — https://cs229.stanford.edu
  - [ ] CS231n Stanford — http://cs231n.stanford.edu
  - [ ] Neural Networks: Zero to Hero (Karpathy) — https://karpathy.ai/zero-to-hero.html
  - [ ] d2l.ai — https://d2l.ai
  - [ ] Spinning Up (OpenAI) — https://spinningup.openai.com

---

# PHASE 1 — Math refresh

**20 avril → 10 mai (3 semaines)**

Objectif : être capable de dériver un gradient, comprendre la SVD sans hésiter, être à l'aise avec les lois de probabilités courantes, maîtriser la descente de gradient et l'entropie croisée.

---

## Semaine 1 — Algèbre linéaire (20–26 avril)

**Objectif** : SVD, valeurs propres, projections, espaces vectoriels — niveau solide.

### Core
- [ ] 3Blue1Brown *Essence of Linear Algebra* — regarder l'intégralité (~3h)
- [ ] MML chapitre 2 (Linear Algebra) — lecture + tous les exos
- [ ] MML chapitre 3 (Analytic Geometry) — lecture + exos ciblés
- [ ] Anki : ajouter 10-15 cartes (définitions + propriétés clés)

### Bonus
- [ ] MIT 18.06 Gilbert Strang — au moins les lectures 1-10
- [ ] MML chapitre 4 (Matrix Decompositions) — focus SVD et décomposition en valeurs propres
- [ ] Implémenter la SVD from scratch en numpy (sans `np.linalg.svd`) — via power iteration

### Journal
```
(à remplir dimanche 26/04)
```

---

## Semaine 2 — Probabilités & statistiques (27 avril – 3 mai)

**Objectif** : MLE, MAP, inférence bayésienne, distributions conjuguées, Gaussienne multivariée.

### Core
- [ ] MML chapitre 6 (Probability and Distributions) — lecture + exos
- [ ] Revoir les lois usuelles (Bernoulli, Binomiale, Gaussienne, Gaussienne multivariée, Exponentielle, Beta, Dirichlet)
- [ ] Dériver à la main :
  - [ ] MLE d'une Gaussienne (μ et σ²)
  - [ ] MAP d'une Bernoulli avec prior Beta
- [ ] Anki : 10-15 cartes

### Bonus
- [ ] Bishop chapitre 1 (Introduction)
- [ ] Bishop chapitre 2 (Probability Distributions) — focus sur les distributions conjuguées
- [ ] Implémenter un échantillonneur Gibbs simple sur un exemple jouet

### Journal
```
(à remplir dimanche 03/05)
```

---

## Semaine 3 — Optimisation + théorie de l'information (4–10 mai)

**Objectif** : convexité, KKT, gradient descent, entropie, KL, cross-entropy.

### Core
- [ ] MML chapitre 7 (Continuous Optimization) — lecture + exos
- [ ] Boyd chapitre 2 (Convex Sets) — lecture
- [ ] Boyd chapitre 3 (Convex Functions) — lecture + exos ciblés
- [ ] Boyd chapitre 9 (Unconstrained Minimization) — focus gradient descent, Newton, convergence
- [ ] Cover & Thomas chapitre 2 (Entropy, Relative Entropy and Mutual Information) — lecture + exos
- [ ] Anki : 10-15 cartes (formules KL, entropie, Jensen, etc.)

### Bonus
- [ ] Boyd chapitre 5 (Duality)
- [ ] Implémenter gradient descent, SGD, et Adam from scratch sur une régression linéaire
- [ ] Comparer leurs courbes de convergence sur un dataset jouet

### Checkpoint de phase 1
Sur feuille blanche, je dois pouvoir :
- [ ] Dériver le gradient de la log-vraisemblance d'une régression logistique
- [ ] Expliquer ce que fait la SVD et pourquoi elle existe toujours
- [ ] Écrire la formule de l'entropie croisée et expliquer pourquoi c'est la bonne loss pour la classification
- [ ] Expliquer la différence MLE / MAP avec un exemple concret

### Journal
```
(à remplir dimanche 10/05)
```

---

# PHASE 2 — ML classique

**11 mai → 21 juin (6 semaines)**

Objectif : maîtriser les fondamentaux de CS 7641 — théorie formelle + implémentation from scratch des algos clés.

**Ressource maîtresse** : CS229 Stanford (les notes de cours détaillées, pas la version Coursera courte). Complément : Bishop ou Murphy selon les sujets.

---

## Semaine 4 — Régression linéaire et logistique (11–17 mai)

### Core
- [ ] CS229 Lecture notes 1 (Supervised Learning, Linear Regression)
- [ ] CS229 Lecture notes 2 (Classification, Logistic Regression)
- [ ] Bishop chapitre 3 (Linear Models for Regression) — sections clés
- [ ] Bishop chapitre 4 (Linear Models for Classification) — sections clés
- [ ] Dériver à la main la formule fermée des moindres carrés et les updates de descente de gradient pour la régression logistique

### Bonus — implémentation from scratch
- [ ] `LinearRegression` (forme fermée + descente de gradient) → push sur repo
- [ ] `LogisticRegression` (descente de gradient + régularisation L2) → push sur repo
- [ ] README de chaque implémentation : théorie, dérivation, résultats sur un dataset sklearn

### Journal
```
```

---

## Semaine 5 — Modèles génératifs + méthodes à noyau (18–24 mai)

### Core
- [ ] CS229 notes sur Generative Learning Algorithms (GDA, Naive Bayes)
- [ ] CS229 notes sur Kernel Methods
- [ ] Bishop chapitre 6 (Kernel Methods) — sections 6.1 et 6.2
- [ ] Comprendre le kernel trick : dériver pourquoi on peut calculer le produit scalaire dans un espace de dimension infinie

### Bonus
- [ ] `GaussianNaiveBayes` from scratch → push sur repo
- [ ] `GaussianDiscriminantAnalysis` from scratch → push sur repo
- [ ] Comparaison générative vs discriminative sur un même dataset

### Journal
```
```

---

## Semaine 6 — SVM, régularisation, bias-variance (25–31 mai)

### Core
- [ ] CS229 notes sur Support Vector Machines (formulation primale + duale)
- [ ] Bishop chapitre 7 (Sparse Kernel Machines) — sections 7.1 SVM
- [ ] CS229 notes sur Regularization and Model Selection
- [ ] Comprendre formellement le tradeoff bias-variance (dérivation)

### Bonus
- [ ] Implémenter un SVM linéaire from scratch (descente sous-gradient sur la hinge loss) → push sur repo
- [ ] Implémenter un SVM avec kernel RBF via SMO simplifié (optionnel, ambitieux)
- [ ] Expérimenter validation croisée k-fold from scratch

### Journal
```
```

---

## Semaine 7 — Arbres et ensembles (1–7 juin)

### Core
- [ ] Bishop chapitre 14 (Combining Models) — focus boosting
- [ ] Murphy sur les arbres de décision et Random Forest
- [ ] Papier AdaBoost original (Freund & Schapire) — dérivation de l'algo
- [ ] XGBoost paper (Chen & Guestrin, 2016) — lecture du chapitre théorique

### Bonus
- [ ] `DecisionTree` from scratch (CART, critère Gini + entropie) → push sur repo
- [ ] `RandomForest` from scratch (par-dessus ton `DecisionTree`) → push sur repo
- [ ] `AdaBoost` from scratch avec stumps → push sur repo

### Journal
```
```

---

## Semaine 8 — Non-supervisé (8–14 juin)

### Core
- [ ] CS229 notes sur K-means, Mixture of Gaussians, EM
- [ ] Bishop chapitre 9 (Mixture Models and EM) — complet
- [ ] CS229 notes sur PCA
- [ ] Bishop chapitre 12 (Continuous Latent Variables) — focus PCA probabiliste

### Bonus
- [ ] `KMeans` from scratch avec k-means++ → push sur repo
- [ ] `GaussianMixtureModel` avec EM from scratch → push sur repo
- [ ] `PCA` from scratch (via SVD) → push sur repo
- [ ] Visualiser MNIST en 2D via PCA vs t-SNE (utiliser sklearn pour t-SNE)

### Journal
```
```

---

## Semaine 9 — Théorie de l'apprentissage + intro RL (15–21 juin)

### Core
- [ ] CS229 notes sur Learning Theory (PAC, VC dimension, bornes de généralisation)
- [ ] CS229 notes sur Reinforcement Learning (MDP, Bellman)
- [ ] Sutton & Barto chapitres 1-4 (Introduction, Multi-armed Bandits, Finite MDPs, Dynamic Programming)

### Bonus
- [ ] Implémenter Q-learning tabulaire sur FrozenLake ou Taxi (gym) → push sur repo
- [ ] Implémenter value iteration et policy iteration from scratch

### Checkpoint de phase 2
- [ ] Mon repo contient au moins 8-10 algos from scratch avec README explicatif
- [ ] Je peux expliquer sans note : bias-variance tradeoff, kernel trick, EM, boosting, VC dimension
- [ ] Je sais quand utiliser quel algo et pourquoi

### Journal
```
```

---

# PHASE 3 — Deep Learning

**22 juin → 26 juillet (5 semaines)**

Objectif : maîtrise PyTorch, compréhension intime des réseaux de neurones, du Transformer, et des modèles génératifs. Aligné CS 7643.

**Ressource maîtresse** : Karpathy *Neural Networks: Zero to Hero* — non-négociable.

---

## Semaine 10 — Backprop et MLP from scratch (22–28 juin)

### Core
- [ ] Karpathy *Zero to Hero* — Lecture 1 (micrograd) : regarder + coder en parallèle
- [ ] Karpathy *Zero to Hero* — Lecture 2 (makemore: bigram) : idem
- [ ] Karpathy *Zero to Hero* — Lecture 3 (makemore: MLP) : idem
- [ ] Karpathy *Zero to Hero* — Lecture 4 (activations, initialization, BatchNorm) : idem
- [ ] Goodfellow chapitre 6 (Deep Feedforward Networks) — lecture

### Point critique
- [ ] Je peux coder la backpropagation from scratch en numpy sans regarder d'exemple. **Si je n'y arrive pas, je m'arrête là et je retravaille jusqu'à y arriver.**

### Bonus
- [ ] Réécrire `micrograd` à ma manière, sans regarder le code de Karpathy
- [ ] Entraîner un MLP sur MNIST en pur numpy (sans PyTorch) → push sur repo

### Journal
```
```

---

## Semaine 11 — PyTorch + CNN (29 juin – 5 juillet)

### Core
- [ ] d2l.ai chapitres 5-7 (Deep Learning Computation, CNN, Modern CNN)
- [ ] CS231n lecture notes sur CNN
- [ ] CS231n assignment 1 (kNN, SVM, softmax, MLP two-layer)
- [ ] Papier AlexNet (Krizhevsky 2012) — lecture
- [ ] Papier ResNet (He 2015) — lecture

### Bonus
- [ ] CS231n assignment 2 (Fully-Connected Nets, BatchNorm, Dropout, CNN)
- [ ] Entraîner un CNN sur CIFAR-10, atteindre >80% test accuracy → push sur repo
- [ ] Implémenter un petit ResNet-18 from scratch en PyTorch

### Journal
```
```

---

## Semaine 12 — RNN, LSTM, attention (6–12 juillet)

### Core
- [ ] Karpathy *Zero to Hero* — Lecture 5 (WaveNet / hierarchical model)
- [ ] d2l.ai chapitre 9 (RNN) et chapitre 10 (Modern RNN: GRU, LSTM)
- [ ] Lecture du blog de Karpathy "The Unreasonable Effectiveness of RNNs"
- [ ] Lecture du papier original sur l'attention (Bahdanau 2014)

### Bonus
- [ ] Implémenter un char-RNN from scratch en PyTorch → push sur repo
- [ ] Implémenter un LSTM cell from scratch

### Journal
```
```

---

## Semaine 13 — Transformers + nanoGPT (13–19 juillet) — **SEMAINE CLÉ**

### Core
- [ ] Karpathy *Zero to Hero* — Lecture 6 (Let's build GPT)
- [ ] Karpathy *Zero to Hero* — Lecture 7 (Let's build the GPT Tokenizer)
- [ ] Papier *Attention is All You Need* (Vaswani 2017) — lecture approfondie, chaque équation
- [ ] d2l.ai chapitre 11 (Attention Mechanisms and Transformers)

### Objectif
- [ ] Avoir codé un Transformer decoder from scratch qui génère du texte cohérent (Shakespeare ou équivalent) — push sur repo avec README détaillé

### Bonus
- [ ] Lecture papier BERT (Devlin 2018)
- [ ] Lecture papier GPT-3 (Brown 2020)
- [ ] Explorer le code de nanoGPT de Karpathy en détail et écrire une note expliquant chaque fichier

### Journal
```
```

---

## Semaine 14 — Modèles génératifs et self-supervised (20–26 juillet)

### Core
- [ ] Bishop chapitre 8 (Graphical Models) — lecture rapide
- [ ] Goodfellow chapitre 20 (Deep Generative Models) — sections VAE et GAN
- [ ] Papier VAE (Kingma 2013)
- [ ] Papier GAN original (Goodfellow 2014)
- [ ] Blog/paper sur diffusion models (Ho 2020, DDPM — au moins lire l'intro et comprendre l'idée)

### Bonus
- [ ] Implémenter un VAE sur MNIST en PyTorch → push sur repo
- [ ] Implémenter un petit GAN sur MNIST → push sur repo

### Checkpoint de phase 3
- [ ] Mon repo contient : MLP from scratch numpy, CNN PyTorch CIFAR-10, char-RNN, Transformer generatif, VAE
- [ ] Je peux expliquer la différence entre attention vs self-attention vs cross-attention
- [ ] Je peux dessiner l'architecture d'un Transformer et expliquer chaque bloc

### Journal
```
```

---

# PHASE 4 — Intensif post-stage + projet final

**27 juillet → 24 août (4 semaines)**

Fin du stage le 27 juillet → je passe à ~30-40h/semaine sur le ML.

---

## Semaine 15 — RL deep (27 juillet – 2 août)

### Core
- [ ] Sutton & Barto chapitres 5-6 (Monte Carlo, Temporal-Difference)
- [ ] Spinning Up (OpenAI) — partie 1 (intro to RL)
- [ ] Spinning Up — partie 2 (key algorithms)
- [ ] Papier DQN (Mnih 2013)
- [ ] Papier PPO (Schulman 2017)

### Bonus
- [ ] Implémenter DQN sur CartPole ou LunarLander → push sur repo
- [ ] Implémenter REINFORCE from scratch

### Journal
```
```

---

## Semaine 16 — Consolidation et choix du projet (3–9 août)

### Core
- [ ] Relire mes notes de phase 1 (math)
- [ ] Relire mes notes de phase 2 (ML classique)
- [ ] Identifier mes 3 zones les plus fragiles et les retravailler
- [ ] Lire 3 papers dans un domaine qui m'attire (LLM / vision / RL / médical)
- [ ] **Choisir le projet final** parmi :
  - Option A : reproduction d'un paper ML en oncologie (lien Oncoshot)
  - Option B : fine-tuning d'un LLM sur corpus médical
  - Option C : projet de zéro (exemple : petit clone ChatGPT domaine étroit)

### Bonus
- [ ] Scoper le projet : dataset, baseline, métriques, timeline sur 3 semaines
- [ ] Setup environnement, premier prototype

### Journal
```
```

---

## Semaines 17-19 — Projet final (10–24 août)

### Jalons projet
- [ ] **Semaine 17** (10-16 août) : baseline qui tourne end-to-end, premiers résultats même médiocres
- [ ] **Semaine 18** (17-23 août) : itération, amélioration, expériences, ablations
- [ ] **Semaine 19** (24 août) : README soigné, blog post, nettoyage du repo, préparation GT

### Livrables
- [ ] Repo GitHub propre, bien documenté
- [ ] README avec : problème, approche, dataset, résultats, limites, next steps
- [ ] Blog post (Medium ou GitHub Pages) expliquant le projet
- [ ] Mise à jour du README principal de `gatech-prep` avec rétrospective des 19 semaines

### Checkpoint final — avant GT
- [ ] Je peux parler 10 minutes sans notes de mon projet
- [ ] Je me sens prêt pour CS 7641 et CS 7643
- [ ] Mon repo GitHub est un bon portfolio

---

# Routine hebdomadaire par défaut

- **Lundi à vendredi (jours de stage)** : 1h à 1h30 le matin ou le soir → lecture, vidéos, exos théoriques (~6h/semaine)
- **Samedi** : 3-4h de coding/implémentation (jour atelier)
- **Dimanche** : 30 min de review — mise à jour du journal, Anki, planning de la semaine suivante

**Total Core : ~8-10h/semaine**

---

# Principes non-négociables

1. Pas une ligne de code ML sans pouvoir expliquer à voix haute ce qu'elle fait.
2. Si je bloque, je retourne à la théorie avant d'aller sur Stack Overflow.
3. Si je rate une semaine Core, je rattrape le weekend suivant — pas de "je verrai plus tard".
4. Chaque dimanche : journal rempli. Non-négociable.
5. Toutes mes implémentations from scratch vont sur le repo, même imparfaites.

---

# Journal global

```
(Semaine 1)

(Semaine 2)

(Semaine 3)

...
```
