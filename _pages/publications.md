---
layout: archive
title: "Research"
permalink: /publications/
author_profile: true
---

My research interests are within the field of Bayesian methods, more specifically:

  - **Variable and structure selection**: projection predictive inference, variable selection for Gaussian Processes etc.
  - **Robust Inference**: Markov Chain Monte Carlo methods (HMC), variational inference, etc.
  - **Bayesian modeling**: multilevel models, additive models, Gaussian Processes, etc.

## Why Bayesian?

When modeling, it is important to have at our disposal principled tools and workflows that help us to build, fit, evaluate and diagnose our models.
A fundamental part of this is the ability of expressing and incorporating our assumptions and prior knowledge into the model itself to carry out inference. 
Indeed, not only do we need robust methods for inference but also efficient and computationally fast ones, since the modeling pipeline is rarely, if ever, implemented only once in a given problem.

To achieve this, I work with the [Stan](http://mc-stan.org) probabilistic language, that uses Hamiltonian Monte Carlo to run inference for our models.
Hamiltonian Monte Carlo is a very efficient MCMC sampler that runs orders of magnitude faster than previous methods.
As such, it is able to converge to the true posterior distribution of the model's parameters very fast, apart from informing the user about any pathological behaviour that may have happened during sampling: a *must* tool to have!

## Current Research

A main part of my current research focuses on the following:

  - **projpred**: [projpred](https://github.com/stan-dev/projpred.git) is an R-package that performs Bayesian variable and structure selection for a given reference model. Our work involves:
    1. Extending projection predictive inference for other classes of models, including additive and linear multilevel models.
    2. Fully rewriting the internals and external API to admit more flexible inputs based of R `formula` objects.
    2. Extending projection predictive inference to models outside of the exponential family, such as ordinal regression models, survival analysis, etc.
  - **robust Variational Inference**: in this project we aim at making variational inference more robust by extending the toolbox of diagnostics available. We are basing this work around the interpretation of the optimization trajectories as stochastic processes converging to a stationary distribution, on which we can now apply a variety of MCMC diagnostics. We have already released a publication that has been accepted to NeurIPS 2020, stay tuned for upcoming work!

## Writing

Here I will post the list of my refereed articles, whereas more informal blog posts will go into [Blog Posts](http://alejandrocatalina.github.io/year-archive/).

Preprints

  - **Catalina A.**, Bürkner P.C., Vehtari A. (2020). Projection Predictive Inference for Generalized Linear and Additive Multilevel Models. [[online](https://arxiv.org/abs/2010.06994)]
  - Paananen T., **Catalina A.**, Bürkner P.C., Vehtari A. (2020). Group Heterogeneity Assessment for Multilevel Models. [[online](https://arxiv.org/abs/2005.02773v1)]

Journal articles

  - **Catalina A.**, Alaíz C.M., Dorronsoro J.R. (2019). Combining Numerical Weather Predictions and Satellite Data for PV Energy Nowcasting, IEEE Transactions on Sustainable Energy. DOI: 10.1109/TSTE.2019.2946621.
  - **Catalina A.**, Torres-Barrán A., Alaíz C.M., Dorronsoro J.R. (2018). Machine Learning Nowcasting of PV Energy using Satellite Data. Neural Processing Letters (NEPL). DOI: 10.1007/s11063-018-09969-1. [[article](https://link.springer.com/article/10.1007/s11063-018-09969-1)]
  
Conference articles
  - Dhaka A.K., **Catalina A.**, Andersen, M.R., Magnusson, M., Huggings, J., Vehtari, A. (2020). Robust, Accurate Stochastic Optimization for Variational Inference. In Neural Information Processing Systems (NeurIPS) 2020, accepted for publication.
  - Ruiz C., **Catalina A.**, Alaíz C.M., Dorronsoro J.R. (2019). Flexible Kernel Selection in Multitask Support VectorRegression. In 2019 International Joint Conference on Neural Networks (IJCNN).
  - de la Pompa V., **Catalina A.**, Dorronsoro J.R. (2018) Gaussian Process Kernels for Support Vector Regression inWind Energy Prediction. In: Yin H., Camacho D., Novais P., Tallón-Ballesteros A. (eds) Intelligent DataEngineering and Automated Learning – IDEAL 2018. IDEAL 2018. Lecture Notes in Computer Science, vol 11315.Springer, Cham. [[article](https://link.springer.com/chapter/10.1007/978-3-030-03496-2_17)]
  - **Catalina A.**, Alaíz C.M., Dorronsoro J.R. (2018). Fused Lasso Dimensionality Reduction of Highly Correlated NWP Features. In: Woon W., Aung Z., Kramer O., Madnick S. (eds) Data Analytics for Renewable Energy Integration. DARE 2018. Lecture Notes in Computer Science. [[article](https://link.springer.com/chapter/10.1007/978-3-030-04303-2_2)]
  - **Catalina A.**, Alaíz C.M., Dorronsoro J.R. (2018). Accelerated Block Coordinate Descent for Sparse Group Lasso. In 2018 International Joint Conference on Neural Networks (IJCNN) (pp. 1-8). IEEE. [[article](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8489078)]
  - **Catalina A.**, Alaíz C.M., Dorronsoro J.R. (2018). Revisiting FISTA for Lasso: Acceleration Strategies Over the Regularization Path. In ESANN 2018. [[article](https://www.semanticscholar.org/paper/Revisiting-FISTA-for-Lasso%3A-Acceleration-Strategies-Catalina-Ala%C3%ADz/4e8c7545da99363624ab58e709bfeaeecbcd1af1)]
  - **Catalina A.**, Dorronsoro J.R. (2017) NWP Ensembles for Wind Energy Uncertainty Estimates. In: Woon W., AungZ., Kramer O., Madnick S. (eds) Data Analytics for Renewable Energy Integration. DARE 2017. Lecture Notes in Computer Science, vol 10691. Springer, Cham. [[article](https://link.springer.com/chapter/10.1007/978-3-319-71643-5_11)]
  - **Catalina A.**, Torres-Barrán A., Dorronsoro J.R. (2017) Satellite Based Nowcasting of PV Energy over Peninsular Spain. In: Rojas I., Joya G., Catala A. (eds) Advances in Computational Intelligence. IWANN 2017. Lecture Notes in Computer Science, vol 10305, pages 685-697. Springer, Cham. [[article](https://link.springer.com/chapter/10.1007/978-3-319-59153-7_59)]
  - **Catalina A.**, Torres-Barrán A., Dorronsoro J.R. (2017) Machine Learning Prediction of Photovoltaic Energy fromSatellite Sources. In: Woon W., Aung Z., Kramer O., Madnick S. (eds) Data Analytics for Renewable Energy Integration. DARE 2016. Lecture Notes in Computer Science, vol 10097, pages 31-42. Springer, Cham. [[article](https://link.springer.com/chapter/10.1007/978-3-319-50947-1_4)]
