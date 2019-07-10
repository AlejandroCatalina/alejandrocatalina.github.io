---
layout: archive
title: "Research"
permalink: /publications/
author_profile: true
---

My research interests are within the field of Bayesian methods, more specifically:

  - **Feature selection**: projective inference, predictive performance, etc.
  - **Inference**: Markov Chain Monte Carlo methods (HMC), variational inference, expectation propagation, Stein variational gradient descent, etc.
  - **Generative models**: manifold learning, flow--based methods, differential modeling (ODE and SDE based models), etc.
  - **Bayesian Modeling**: multilevel models, etc.

## Why Bayesian?

When modeling it is important to have at our disposal principled tools and workflows that help us to build, fit, evaluate and diagnose our models.
A fundamental part of this is the ability of expressing and incorporating our assumptions and prior knowledge into the model itself to carry out inference. 
Indeed, not only do we need robust methods for inference but also efficient and computationally fast ones, since the modeling pipeline is rarely, if ever, implemented only once in a given problem.

To achieve this, I work with the [Stan](http://mc-stan.org) probabilistic language, that uses Hamiltonian Monte Carlo to run inference for our models.
Hamiltonian Monte Carlo is a very efficient MCMC sampler that runs orders of magnitude faster than previous methods.

## Current Research

A main part of my current research focuses on the following:

  - **projpred**: [projpred](https://github.com/stan-dev/projpred.git) is an R-package that performs Bayesian feature selection for a given reference model. My main projects right now consist on 
    1. extending and improving the current projpred's API to work on `formula` objects, making projpred a much more general package and,
    2. extending projpred to work on more types of models, from Generalized Additive Models to more complex multilevel models, that require developing new theory.
  - **diffGP**: in this project a colleague and I are implementing the ideas in [Differentially deep Gaussian processes](https://arxiv.org/abs/1810.04066) and trying to improve upon some of its limitations, for instance implementing a better inference algorithm.

## Writing

Here I will post the list of my refereed articles, whereas more informal blog posts will go into [Blog Posts](http://alejandrocatalina.github.io/year-archive/).

Journal articles

  - ...
  - ...
  
Conference articles

  - ...
  - ...
