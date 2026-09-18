---
title: Enhancing fMRI Data Decoding with Spatiotemporal Characteristics in Limited Dataset
weight: 40
year: 2025
venue: Doklady Mathematics
authors: "**Daniil Dorin**, Andrey Grabovoy, Vadim Strijov"
affiliations: "Antiplagiat Company, Moscow; Forecsys, Moscow"
cover: method.png
coverContain: true
summary: Subject-specific brain activity masks from cross-correlation plus a Riemannian-geometry encoder. Beats neural-network baselines on fMRI classification when data is scarce.
tags: [fMRI, Riemannian geometry, small data]
links:
  - name: Paper
    url: https://link.springer.com/article/10.1134/S1064562425700383
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
    journal   = {Doklady Rossijskoj Akademii Nauk. Mathematika, Informatika, Processy Upravlenia},
    volume    = {527},
    pages     = {11--30},
    year      = {2025},
    publisher = {Russian Academy of Sciences}
  }
---

Deep networks struggle on fMRI: few samples per subject, high variability, heavy compute. This paper asks what works when data is scarce.

![Task: classify the viewed stimulus from a subject's fMRI time series.](task.png)

## Method

- **Brain Activity Decoder.** For each stimulus class, cross-correlate every voxel's time series with the stimulus timeline and keep the most responsive voxels as a binary activity mask. Masks are subject-specific and cut the spatial dimensionality by orders of magnitude.
- **Riemannian encoder.** Covariance matrices of the masked signals are mapped to the tangent space of the SPD manifold, producing spatiotemporal features that a simple classifier consumes.

![Method: per-class activity masks → Riemannian spatiotemporal features → classifier.](method.png)

## Results

On six subjects the method outperforms neural-network baselines, and the gap widens as the training set shrinks. An ablation shows a significant quality drop when either the masks or the Riemannian encoder is removed. Presented at AI Journey 2025.
