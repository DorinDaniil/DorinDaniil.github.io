---
title: "Forecasting fMRI Images From Video Sequences: Linear Model Analysis"
weight: 50
year: 2024
venue: Health Information Science and Systems, 12:55
authors: "**Daniil Dorin**\\*, Nikita Kiselev\\*, Andrey Grabovoy, Vadim Strijov (\\* equal contribution)"
affiliations: "Forecsys, Moscow; Innopolis University; Antiplagiat Company"
cover: overview.jpg
coverContain: true
summary: A per-voxel linear autoregressive model predicts the next fMRI volume from ResNet152 embeddings of the video a person is watching. The best delay matches the hemodynamic lag.
tags: [fMRI, video, linear models]
links:
  - name: Paper
    url: https://doi.org/10.1007/s13755-024-00315-5
    icon: paper
  - name: Code
    url: https://github.com/DorinDaniil/Forecasting-fMRI-Images
    icon: code
  - name: Poster
    url: https://github.com/DorinDaniil/Forecasting-fMRI-Images/blob/main/poster/poster.pdf
    icon: poster
  - name: Talk
    url: https://www.youtube.com/live/WnIRaRl730A?t=4305
    icon: video
bibtex: |
  @article{dorin2024forecasting,
    author  = {Dorin, Daniil and Kiselev, Nikita and Grabovoy, Andrey and Strijov, Vadim},
    title   = {Forecasting fMRI images from video sequences: linear model analysis},
    journal = {Health Information Science and Systems},
    volume  = {12},
    number  = {1},
    pages   = {55},
    year    = {2024},
    doi     = {10.1007/s13755-024-00315-5}
  }
---

Can a linear model predict the next fMRI volume from the video a person is watching? Video frames are embedded with ResNet152 and an L2-regularised linear regression is fit **per voxel**, assuming a time-invariant hemodynamic response and a Markov property on the image sequence. The model forecasts the difference between consecutive fMRI tensors from a delayed frame embedding.

![Pipeline: ResNet152 frame embeddings and normalised fMRI tensors feed a per-voxel linear regression on the tensor difference.](overview.jpg)

Experiments on a large multi-subject dataset show the best predictive delay is about five seconds, matching the known hemodynamic lag, and that occipital voxels respond predictably to visual content. Model weights are tested for invariance across subjects. The poster version, with voxel weighing, was shown at Neuroinformatics 2024.
