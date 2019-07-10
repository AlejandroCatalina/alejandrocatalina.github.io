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
As such, it is able to converge to the true posterior distribution of the model's parameters very fast, apart from informing the user about any pathological behaviour that may have happened during sampling: a *must* tool to have!

## Current Research

A main part of my current research focuses on the following:

  - **projpred**: [projpred](https://github.com/stan-dev/projpred.git) is an R-package that performs Bayesian feature selection for a given reference model. My main projects right now consist on 
    1. extending and improving the current projpred's API to work on `formula` objects, making projpred a much more general package and,
    2. extending projpred to work on more types of models, from Generalized Additive Models to more complex multilevel models, that require developing new theory.
  - **diffGP**: in this project a colleague and I are implementing the ideas in [Differentially deep Gaussian processes](https://arxiv.org/abs/1810.04066) and trying to improve upon some of its limitations, for instance implementing a better inference algorithm.

## Writing

Here I will post the list of my refereed articles, whereas more informal blog posts will go into [Blog Posts](http://alejandrocatalina.github.io/year-archive/).

Journal articles

  - **Catalina A.**, Alaíz C.M., Dorronsoro J.R. (2019). Combining Numerical Weather Predictions and Satellite Data forPV Energy Nowcasting, *submitted* to IEEE Transactions on Sustainable Energy.
  - **Catalina A.**, Torres-Barrán A., Alaíz C.M., Dorronsoro J.R. (2018). Machine Learning Nowcasting of PV Energyusing Satellite Data. Neural Processing Letters (NEPL). DOI: 10.1007/s11063-018-09969-1.
  
Conference articles

  - Ruiz C., **Catalina A.**, Alaíz C.M., Dorronsoro J.R. (2019). Flexible Kernel Selection in Multitask Support VectorRegression. In 2019 International Joint Conference on Neural Networks (IJCNN), in press.
  - de la Pompa V.,**Catalina A.**, Dorronsoro J.R. (2018) Gaussian Process Kernels for Support Vector Regression inWind Energy Prediction. In: Yin H., Camacho D., Novais P., Tallón-Ballesteros A. (eds) Intelligent DataEngineering and Automated Learning – IDEAL 2018. IDEAL 2018. Lecture Notes in Computer Science, vol 11315.Springer, Cham.
  - **Catalina A.**, Alaíz C.M., Dorronsoro J.R. (2018). Fused Lasso Dimensionality Reduction of Highly Correlated NWPFeatures. In: Woon W., Aung Z., Kramer O., Madnick S. (eds) Data Analytics for Renewable Energy Integration. DARE 2018. Lecture Notes in Computer Science.
  - **Catalina A.**, Alaíz C.M., Dorronsoro J.R. (2018). Accelerated Block Coordinate Descent for Sparse Group Lasso. In 2018 International Joint Conference on Neural Networks (IJCNN) (pp. 1-8). IEEE.
  - **Catalina A.**, Alaíz C.M., Dorronsoro J.R. (2018). Revisiting FISTA for Lasso: Acceleration Strategies Over the Regularization Path. In ESANN 2018.
  - **Catalina A.**, Dorronsoro J.R. (2017) NWP Ensembles for Wind Energy Uncertainty Estimates. In: Woon W., AungZ., Kramer O., Madnick S. (eds) Data Analytics for Renewable Energy Integration. DARE 2017. Lecture Notes in Computer Science, vol 10691. Springer, Cham.
  - **Catalina A.**, Torres-Barrán A., Dorronsoro J.R. (2017) Satellite Based Nowcasting of PV Energy over PeninsularSpain. In: Rojas I., Joya G., Catala A. (eds) Advances in Computational Intelligence. IWANN 2017. Lecture Notes in Computer Science, vol 10305, pages 685-697. Springer, Cham.
  - **Catalina A.**, Torres-Barrán A., Dorronsoro J.R. (2017) Machine Learning Prediction of Photovoltaic Energy fromSatellite Sources. In: Woon W., Aung Z., Kramer O., Madnick S. (eds) Data Analytics for Renewable Energy Integration. DARE 2016. Lecture Notes in Computer Science, vol 10097, pages 31-42. Springer, Cham.
