---
title: Pairwise Image Matching for Plagiarism Detection
weight: 30
year: 2025
venue: Doklady Mathematics
authors: "**Daniil Dorin**, Kseniia Varlamova, Andrey Grabovoy"
cover: method.png
coverContain: true
summary: A siamese network with a weight-shared encoder, symmetric fusion and a similarity head, trained with plagiarism-mimicking augmentations to minimise false positives in pairwise image plagiarism detection.
tags: [image matching, siamese network, plagiarism detection]
links:
  - name: Paper
    url: https://doi.org/10.1134/S1064562425700486
    icon: paper
  - name: Code
    url: https://github.com/DorinDaniil/Pairwise-Image-Matching
    icon: code
bibtex: |
  @article{dorin2025pairwise,
    title     = {Pairwise image matching for plagiarism detection},
    author    = {Dorin, Daniil Dmitrievich and Varlamova, K. D. and Grabovoy, Andrey Valerievich},
    journal   = {Doklady Mathematics},
    volume    = {112},
    number    = {2},
    pages     = {370--381},
    year      = {2025},
    publisher = {Springer}
  }
---

Plagiarism detection represents a critical task across various fields, including academic publishing, journalism, e-commerce, and media verification. While substantial attention focuses on identifying textual plagiarism, image plagiarism, particularly in biology and medicine, remains a significant concern. Automated retrieval systems often surface numerous potential candidates, but a high rate of false positives — pairs incorrectly flagged as plagiarism — necessitates highly accurate pairwise matching for verification. Manual alterations to images, such as rotations, mirroring, conversion to grayscale, and color distortion constitute forms of plagiarism. This work addresses the critical need for false positive rate (FPR) minimization in pairwise image plagiarism detection through rigorous analysis of similarity scoring models. The proposed approach employs a siamese network with three key components: a weight-shared encoder, a symmetric fusion module with order-invariant embedding combination, and a similarity classification head. Training employs a hybrid self-supervised strategy with plagiarism-mimicking augmentations, combining cross-entropy loss and contrastive regularization. Ablation studies evaluate encoder architectures and fusion strategies. For comparison, identical siamese architectures utilize frozen state-of-the-art self-supervised representations Barlow Twins and CLIP, with fusion modules and classification heads trained identically. Experimental validation across multi-domain images demonstrates that end-to-end trained models consistently outperform approaches using frozen state-of-the-art representations.

![Siamese architecture: weight-shared encoders, symmetric fusion module, similarity classification head.](method.png)
