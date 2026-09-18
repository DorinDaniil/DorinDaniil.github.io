---
title: Pairwise Image Matching for Plagiarism Detection
weight: 30
year: 2025
venue: Doklady Mathematics, 112(2)
authors: "**Daniil Dorin**, Kseniia Varlamova, Andrey Grabovoy"
affiliations: "Antiplagiat Company, Moscow"
cover: task.png
coverContain: true
summary: A Siamese network that separates near-duplicates (one image manually derived from another) from merely similar images in scientific publications, robust to rotation, cropping, grayscale, contrast, blur and noise.
tags: [image matching, Siamese network, plagiarism detection]
links:
  - name: Paper
    url: https://link.springer.com/article/10.1134/S1064562425700486
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

Two microscopy images of different cells can look almost identical. A grayscale, cropped copy of one figure can look quite different. Retrieval systems rank by visual similarity and get both cases wrong. We train a **Siamese network** to answer the right question: was the second image manually derived from the first?

![Near-duplicate (derived) vs. merely similar (distinct source).](task.png)

## Architecture

- **Encoders:** EfficientNet-B3, ViT-L/16, CLIP ViT-H/14, or a Barlow Twins ResNet50. Some are kept frozen to compare our training with off-the-shelf contrastive representations.
- **Fusion:** a symmetric function of the two embeddings, so the score does not depend on input order.
- **Head:** an MLP with one hidden layer, ReLU and dropout, ending in a sigmoid that outputs the probability of a near-duplicate relation.

![Siamese encoder → symmetric fusion → near-duplicate probability.](method.png)

The system handles rotations, mirroring, grayscale conversion, contrast changes, cropping, resizing, blur, noise and their combinations. It is the matching stage of the image-search pipeline for plagiarism detection in scientific publishing.
