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
Although my interest comes from the Bayesian methods perspective, it is important to know that these methods are not uniquely Bayesian (note GANs, that are precisely the State of the Art in this field).

  - **Only Bayes should learn a Manifold (on the estimation of differential geometric structure from data)** by Søren Hauberg [[preprint](https://arxiv.org/abs/1806.04994)] *to read*. I found this a very interesting paper that approaches the density estimation problem from a manifold learning perspective and sheds some light from this different angle. Apart from this, it seems to be quite rigorous on the math.
  - **Density estimation using Real NVP** by Laurent Dinh, Jascha Sohl-Dickstein and Samy Bengio [[preprint](http://arxiv.org/abs/1605.08803)]. This paper builds upon a series of articles that work on normalizing flows methods and take them to a new level having very good results at the time. The contribution of this paper is to introduce a new set of invertible non-volume preserving transformations with the benefit of exact log likelihood and exact sampling and inference.
  - **Glow: Generative Flow with Invertible 1x1 Convolutions** by Diederik P. Kingma and Prafulla Dhariwal [[preprint](http://arxiv.org/abs/1807.03039)]. Glow builds on top of real NVP, introducing invertible convolutions as the novelty, showing a significant improvement in terms of test log likelihood. 
  - **FFJORD: Free-form Continuous Dynamics for Scalable Reversible Generative Models** by Will Grathwohl, Ricky T.Q. Chen, Jesse Bettencourt, Ilya Sutskever and David Duvenaud [[article](https://openreview.net/pdf?id=rJxgknCcK7)]. This very recent paper extends both Neural ODEs and real NVP adding two contributions. First, they introduce free form invertible transformations, that add a lot more flexibility to the model. Second, this is possible thanks to the application of continuous time modeling, an idea taken from Neural ODEs.
  - **Neural Ordinary Differential Equations** by Tian Qi Chen, Yulia Rubanova, Jesse Bettencourt and David Duvenaud [[article](http://papers.nips.cc/paper/7892-neural-ordinary-differential-equations.pdf)]. In this paper the authors introduce a whole new class of neural networks that, instead of specifying a discrete set of layers, parameterizes the derivative of the hidden state with a neural net, achieving *continuous depth* models with very nice computational properties.
