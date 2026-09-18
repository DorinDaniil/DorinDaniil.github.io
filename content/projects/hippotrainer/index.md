---
title: "HippoTrainer: gradient-based hyperparameter optimization"
weight: 20
year: 2025
stars: 11
cover: logo.svg
coverContain: true
summary: A PyTorch library that tunes hyperparameters by differentiating through the training loop. Implements T1-T2, Neumann-series implicit differentiation, HOAG and DrMAD behind one trainer interface.
tags: [PyTorch, library, optimization]
links:
  - name: GitHub
    url: https://github.com/intsystems/hippotrainer
    icon: github
  - name: Documentation
    url: https://intsystems.github.io/hippotrainer/
    icon: docs
---

Grid and random search treat the model as a black box. `hippotrainer` instead uses automatic differentiation to compute hypergradients and update hyperparameters with gradient steps, directly on `torch.nn.Module` models.

## Algorithms

- **T1-T2**: one-step unrolled optimisation
- **Neumann**: implicit differentiation via a Neumann-series approximation of the inverse Hessian
- **HOAG**: implicit differentiation with conjugate gradient
- **DrMAD**: memory-efficient piecewise-linear backpropagation through the training trajectory

Checkpointing and implicit differentiation keep memory bounded, so the same code runs on a laptop and on a cluster. Built within the Bayesian Multimodeling course at MIPT.
