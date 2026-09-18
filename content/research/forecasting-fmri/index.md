---
title: "Forecasting fMRI Images From Video Sequences: Linear Model Analysis"
weight: 50
year: 2024
venue: Health Information Science and Systems
authors: "**Daniil Dorin**\\*, Nikita Kiselev\\*, Andrey Grabovoy, Vadim Strijov"
cover: overview.jpg
coverContain: true
summary: A method for approximating fMRI readings from the video sequence a person watches, based on a linear model for each voxel and a time-invariant hemodynamic response.
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
  - name: Video
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

The issue of reconstructing the relationship between functional magnetic resonance imaging (fMRI) sensor readings and human perception of the external is investigated. The study analyzes the dependence between the fMRI images and the videos viewed by individuals. Based on this analysis, a method is proposed for approximating the fMRI readings using the video sequence. The method is based on the assumption that there is a time-invariant hemodynamic response to changes in blood oxygen levels. A linear model is constructed for each individual voxel in the fMRI image, assuming that the image sequence follows a Markov property. To test the proposed method, a computational experiment was conducted on a dataset collected during tomographic examinations of a large number of individuals. The performance of the method was evaluated based on the experimental data, and hypotheses were tested regarding the invariance of the model weights and the correctness of the method.

![Overview of the method: preprocessing of video and fMRI data, and per-voxel linear forecasting.](overview.jpg)
