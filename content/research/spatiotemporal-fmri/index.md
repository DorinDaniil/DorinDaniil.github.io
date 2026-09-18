---
title: Enhancing fMRI Data Decoding with Spatiotemporal Characteristics in Limited Dataset
weight: 40
year: 2025
venue: Doklady Mathematics
authors: "**Daniil Dorin**, Andrey Grabovoy, Vadim Strijov"
cover: method.png
coverContain: true
summary: An fMRI decoding methodology for small datasets that combines subject-specific brain activity masks with an encoder based on Riemannian geometry.
tags: [fMRI, Riemannian geometry, limited data]
links:
  - name: Paper
    url: https://doi.org/10.1134/S1064562425700383
    icon: paper
  - name: Code
    url: https://github.com/DorinDaniil/Spatial-and-Temporal-Characteristics
    icon: code
  - name: Poster
    url: https://github.com/DorinDaniil/Spatial-and-Temporal-Characteristics/blob/main/assets/aij_poster.pdf
    icon: poster
  - name: Video
    url: https://drive.google.com/file/d/13XwQ1Vhpog0QV_kDNLxPBhvNRJp__8BN/view
    icon: video
bibtex: |
  @article{dorin2025enhancing,
    title     = {Enhancing fMRI data decoding with spatiotemporal characteristics in limited dataset},
    author    = {Dorin, Daniil Dmitrievich and Grabovoy, Andrey Valerievich and Strijov, Vadim},
    journal   = {Doklady Mathematics},
    year      = {2025},
    publisher = {Springer}
  }
---

This study investigates the impact of spatiotemporal characteristics on the quality of the decoding of functional Magnetic Resonance Imaging (fMRI) data. Neural network architectures are limited in handling fMRI data due to the small sample size, high sample variability, and significant computational resources required. We propose a methodology for fMRI decoding with an insufficient dataset. We examine the unique structural features of each subject's brain. To build a decoding methodology, we propose an algorithm for extracting a unique activity mask from the brain for each subject. This algorithm reduces the spatial dimensionality of fMRI time series through weighting stimulated brain regions using cross-correlation. We developed a classification model for the fMRI time series data from a single subject. It combines two parts: the first part is the brain activity masks extracted for each activity class using the extraction algorithm. The second part is an encoder that employs Riemannian geometry to extract spatiotemporal characteristics. The computational experiment analyzes the proposed methodology on a sample obtained from tomographic examinations of six subjects. An ablation analysis of the proposed classification model shows a significant decrease in quality when any component of the model is missing. Comparisons with neural network-based approaches demonstrate the superior performance of the proposed methodology, especially in scenarios with limited data.

![Overview of the proposed classification model: per-class activity masks and a Riemannian spatiotemporal encoder.](method.png)

![Riemannian geometry of SPD matrices: logarithmic and exponential maps between the manifold and the tangent space at the reference point.](riemannian.png)
