---
title: Decentralized Optimization with Coupled Constraints
weight: 60
year: 2025
venue: ICLR 2025
math: true
authors: "Demyan Yarmoshik, Alexander Rogozin, Nikita Kiselev, **Daniil Dorin**, Alexander Gasnikov, Dmitry Kovalev"
cover: plot.png
coverContain: true
summary: Lower complexity bounds for decentralized optimization with affine coupled constraints, and the first linearly convergent first-order decentralized algorithm that achieves them.
tags: [optimization, decentralized, convex]
links:
  - name: OpenReview
    url: https://openreview.net/forum?id=AJM52ygi6Y
    icon: paper
  - name: arXiv
    url: https://arxiv.org/abs/2407.02020
    icon: paper
bibtex: |
  @inproceedings{yarmoshik2025decentralized,
    title     = {Decentralized Optimization with Coupled Constraints},
    author    = {Yarmoshik, Demyan and Rogozin, Alexander and Kiselev, Nikita and Dorin, Daniil and Gasnikov, Alexander and Kovalev, Dmitry},
    booktitle = {The Thirteenth International Conference on Learning Representations (ICLR)},
    year      = {2025},
    url       = {https://openreview.net/forum?id=AJM52ygi6Y}
  }
---

We consider the decentralized minimization of a separable objective $\sum_{i=1}^{n} f_i(x_i)$, where the variables are coupled through an affine constraint $\sum_{i=1}^n\left(\mathbf{A}_i x_i - b_i\right) = 0$. We assume that the functions $f_i$, matrices $\mathbf{A}_i$, and vectors $b_i$ are stored locally by the nodes of a computational network, and that the functions $f_i$ are smooth and strongly convex. This problem has significant applications in resource allocation and systems control and can also arise in distributed machine learning. We propose lower complexity bounds for decentralized optimization problems with coupled constraints and a first-order algorithm achieving the lower bounds. To the best of our knowledge, our method is also the first linearly convergent first-order decentralized algorithm for problems with general affine coupled constraints.

![Convergence of the proposed method compared with baselines.](plot.png)
