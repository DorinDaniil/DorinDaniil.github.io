---
title: "Just Relax It: discrete variable relaxation"
weight: 10
year: 2025
stars: 26
cover: overview.png
coverContain: true
summary: PyTorch library of relaxation methods for discrete random variables in neural networks. Gumbel-Softmax Top-K, Hard Concrete, Straight-Through Bernoulli, Invertible Gaussian, REBAR and more, behind a Pyro-style distribution API.
tags: [PyTorch, library]
links:
  - name: GitHub
    url: https://github.com/intsystems/relaxit
    icon: github
  - name: Documentation
    url: https://intsystems.github.io/relaxit/
    icon: docs
---

Sampling discrete random variables inside a neural network breaks gradient flow. The usual fix, Gumbel-Softmax, is only one of many relaxations. `relaxit` collects the alternatives in a single PyTorch-compatible package with a distribution interface modelled on `torch.distributions` and Pyro.

![Discrete distributions and their continuous relaxations.](overview.png)

## Implemented distributions

- Relaxed Bernoulli and Correlated Relaxed Bernoulli
- Gumbel-Softmax Top-K and Generalized Gumbel-Softmax
- Straight-Through Bernoulli, Stochastic Times Smooth
- Invertible Gaussian with a closed-form KL
- Hard Concrete
- Logistic-Normal and a Laplace-form approximation of the Dirichlet
- REBAR

The repository ships with tests, coverage, a demo notebook with VAE experiments on MNIST, and a technical report. Built within the Bayesian Multimodeling course at MIPT.
