---
layout: archive
title: "To read"
permalink: /to-read/
author_profile: true
---

I attend regularly some reading circles here at Aalto and in this page I will post a list of papers and resources that I find useful or interesting or that I intend to read and study.
It is very likely that I miss a lot of good references, and any of these misses will be intentional, so take this as a list of my favourites.
As a collateral effect, if any of the papers or references that I post here remind you of some good references that I haven't posted here, please drop me an email as I would definitely like to take a look at those.

## Journal Club

Most of the papers that I will post here are very related to my research interests, that you can read about at [Research](http://alejandrocatalina.github.io), although some of the papers may be here more as a general reference.
The two reading circles that currently I attend are *Variational Inference* and *Deep Generative Models*, self organized by students at the PML group here at Aalto, so many of these papers will be related to those.

### Generative Models

This collection of papers is related to generative models, where our aim is to learn the underlying distribution of a given data sample with the ultimate goal of *generating* samples from this distribution.
Although my interest comes from the Bayesian perspective, it is important to know that these methods are not uniquely Bayesian (note GANs, that are precisely the State of the Art in this field).

  - **Only Bayes should learn a Manifold (on the estimation of differential geometric structure from data)** by Søren Hauberg [[preprint](https://arxiv.org/abs/1806.04994)] *to read*. I found this a very interesting paper that approaches the density estimation problem from a manifold learning perspective and sheds some light from this different angle. Apart from this, it seems to be quite rigorous on the math.
  - **Variational Implicit Processes** by Chao Ma, Yingzhen Li, José Miguel Hernández Lobato [[preprint](http://arxiv.org/abs/1806.02390)]. Here the authors introduce *Implicit Processes*, a stochastic process that places implicit multivariate distributions over collections of random variables. These are highly flexible implicit priors over functions. They also propose a novel inference algorithm for these models.
  - **Deep learning with differential Gaussian process flows** by Pashupati Hegde, Markus Heinonen, Harri Lähdesmäki and Samuel Kaski [[preprint](https://arxiv.org/abs/1810.04066)]. Here the authors present a very similar approach to Neural ODEs to the case of Gaussian Processes. They model the dynamics of an Stochastic Differential Equation with a GP and integrate it with an Euler-Maruyama solver. In turn, they achieve continuous--depth gaussian processes in a similar fashion as Neural ODEs. They use DSVI (Doubly Stochastic Variational Inference) for inference.
  - **FFJORD: Free-form Continuous Dynamics for Scalable Reversible Generative Models** by Will Grathwohl, Ricky T.Q. Chen, Jesse Bettencourt, Ilya Sutskever and David Duvenaud [[article](https://openreview.net/pdf?id=rJxgknCcK7)]. This very recent paper extends both Neural ODEs and real NVP adding two contributions. First, they introduce free form invertible transformations, that add a lot more flexibility to the model. Second, this is possible thanks to the application of continuous time modeling, an idea taken from Neural ODEs.
  - **Glow: Generative Flow with Invertible 1x1 Convolutions** by Diederik P. Kingma and Prafulla Dhariwal [[preprint](http://arxiv.org/abs/1807.03039)]. Glow builds on top of real NVP, introducing invertible convolutions as the novelty, showing a significant improvement in terms of test log likelihood. 
  - **Neural Ordinary Differential Equations** by Tian Qi Chen, Yulia Rubanova, Jesse Bettencourt and David Duvenaud [[article](http://papers.nips.cc/paper/7892-neural-ordinary-differential-equations.pdf)]. In this paper the authors introduce a whole new class of neural networks that, instead of specifying a discrete set of layers, parameterizes the derivative of the hidden state with a neural net, achieving *continuous depth* models with very nice computational properties.
  - **Density estimation using Real NVP** by Laurent Dinh, Jascha Sohl-Dickstein and Samy Bengio [[preprint](http://arxiv.org/abs/1605.08803)**. This paper builds upon a series of articles that work on normalizing flows methods and take them to a new level having very good results at the time. The contribution of this paper is to introduce a new set of invertible non-volume preserving transformations with the benefit of exact log likelihood and exact sampling and inference.

### Inference

These articles focus more on the inference methods we use to do inference, looking for better efficiency, computational improvements or maybe a new theoretical approach.

  - **A Conceptual Introduction to Hamiltonian Monte Carlo** by Michael Betancourt [[preprint](http://arxiv.org/abs/1701.02434)] *to-read*. This paper presents a very thorough introduction to Hamiltonian Monte Carlo, the state of the art sampler for Bayesian inference.
  - **Monte Carlo Gradient Estimation in Machine Learning** by Shakir Mohamed, Mihaela Rosca, Michael Figurnov and Andriy Mnih [[preprint](http://arxiv.org/abs/1906.10652)] *to-read*. A very broad and accessible survey on Monte Carlo gradient estimation techniques: the problem of computing the gradient of an expectation of a function with respect to its parameters.
  - **Inference in Deep Gaussian Processes using Stochastic Gradient Hamiltonian Monte Carlo** by Marton Havasi, José Miguel Hernández-Lobato and Juan José Murillo-Fuentes [[preprint](https://arxiv.org/abs/1806.05490)]. Following up the DSVI paper, the authors propose a new inference method to deal with the non gaussianity in the true posterior of Deep GPs. The key of this new method is that it uses stochastic gradient Hamiltonian Monte Carlo (SG-HMC) to approximate the true variational posterior without further assumptions, allowing for yet more flexible variational distributions that improve inference.
  - **Doubly Stochastic Variational Inference for Deep Gaussian Processes** by Hugh Salimbeni and Marc Deisenroth [[preprint](http://arxiv.org/abs/1705.08933)]. In this paper the authors present a new inference method to deal with the between layers correlations present in deep gaussian processes, adding greater flexibility to the models but also a higher computational cost, as in this case it is no longer possible to have an analytical expression for the variational distribution.

### Projective Feature Selection

These articles are directly related to one of my main projects for my PhD. 
They elaborate on the subject of performing feature selection starting from a reference model that is fitted using all the available features.
The algorithm then projects the reference posterior to a subset of features and chooses the best subset at every iteration according to some predictive performance measures; the *elpd* (expected log predictive density).

  - **Projective Inference in High-dimensional Problems: Prediction and Feature Selection** by Juho Piironen, Markus Paasinimei and Aki Vehtari [[preprint](http://arxiv.org/abs/1810.02406)]. This is the full paper describing the theoretical approach. The key point is solving the Maximum Likelihood Estimation problem for each projection. At this point, this only extends to the family of Generalized Linear Models.
  - **The Kernel Interaction Trick: Fast Bayesian Discovery of Pairwise Interactions in High Dimensions** by Raj Agrawal, Jonathan H. Huggins, Brian Trippe and Tamara Broderick [[preprint](http://arxiv.org/abs/1905.06501)]. Very interesting book that introduces a new approach to discover high dimensional interaction effects. This consists of writing the original model as a GP and deriving the equivalent *interaction kernel* for the model and doing inference on the GP instead because the kernel has issues with the sample size not wit the parameter size and in this kind of problems we usually have an scenario where $p \gg N$.
  - **Hierarchical Shrinkage Priors for Regression Models** by Jim Griffin and Phil Brown [[article](http://projecteuclid.org/euclid.ba/1453211963)]. A broad introduction to hierarchical shrinkage priors from a very general perspective.
  - **Projection predictive model selection for Gaussian processes** by Juho Piironen and Aki Vehtari [[article](https://rc.signalprocessingsociety.org/conference-workshop-videos/mlsp/SPSVID00114.html)][[preprint](https://arxiv.org/abs/1510.04813)]. In this paper the authors extend *projpred* for Gaussian Processes, analyzing the problem of the Maximum Likelihood Estimation and proposing a solution with nice experiments comparing to the standard Automatic Relevance Determination approach.
  - **Sparsity information and regularization in the horseshoe and other shrinkage priors** by Juho Piironen and Aki Vehtari [[article](https://projecteuclid.org/euclid.ejs/1513306866)]. The authors propose a new shrinkage prior based on the horseshoe prior, the *regularised* horseshoe prior, that allows identification of large slopes alongside a strong shrinkage of the non relevant ones. 

## Tutorials and Case Studies

In this section I will post a list of more informal references that I found nonetheless useful, maybe from a more practical prespective:

  - **Towards a principled Bayesian workflow** by Michael Betancourt [[link](https://betanalpha.github.io/assets/case_studies/principled_bayesian_workflow.html)]. In this case study Michael explores different options for doing sparse modeling, a very common and popular approach for Generalized Linear Models with high dimensionality. Furthermore, I find everything that Michael writes highly relevant.
  - **Stan User's Guide** by Stan development team [[link](https://mc-stan.org/docs/2_19/stan-users-guide/index.html)]. A must if you are using Stan to write your models, don't miss the language reference either!


## Books

I think these textbooks are really nice material to get into Bayesian statistics and modeling:

  - **Statistical Rethinking** by Richard McElreath [[book](http://xcelab.net/rm/statistical-rethinking/)]. A very nice book about Bayesian modeling, very accessible and covering a broad range of models within Generalized Linear Models, interaction models and finally multilevel models, unleashing very powerful and flexible methods. I particularly loved Richard's style that makes the book very fun to read while learning a lot of interesting concepts like entropy, information criteria, multilevel models, etc.
  - **Bayesian Data Analysis** by Andrew Gelman, John Carlin, Hal Stern, David Dunson, Aki Vehtari, and Donald Rubin [[book](http://www.stat.columbia.edu/~gelman/book/)] *to read*. Another interesting textbook covering some of the same topics Statistical Rethinking does, but from a slightly different perspective. I am taking BDA course at Aalto this fall so I haven't read the book yet.
