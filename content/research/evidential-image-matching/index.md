---
title: "Evidential Image Matching: Predicting Transformation Sequences to Derive One Image from Another"
weight: 20
year: 2026
venue: Computer Vision and Image Understanding
status: under review
authors: "**Daniil Dorin**, Kseniia Varlamova, Andrey Grabovoy"
cover: card.png
coverContain: true
summary: Plagiarism detection reformulated as predicting the sequence of transformations that derives one image from another, with an encoder–decoder model and the Canonical Jaccard Index.
tags: [image matching, plagiarism detection, encoder–decoder]
links:
  - name: Code
    url: https://github.com/DorinDaniil/Image-Transform-Predict
    icon: code
---

Detecting image plagiarism and near-duplicate content remains a critical challenge in academic publishing, media verification, and e-commerce. Existing methods typically rely on pairwise similarity scores, which provide limited interpretability and often struggle to distinguish visual similarity from true transformational derivability. To address this limitation, we reformulate the problem as *evidential image matching*: given a reference image and a suspect image, the model predicts the sequence of transformations that derives one image from the other. An empty sequence indicates non-plagiarism. We propose an encoder-decoder architecture trained to recover transformation sequences from a predefined vocabulary. We further introduce the Canonical Jaccard Index, a reconstruction metric that accounts for equivalent transformation sequences by respecting the algebraic structure of the dihedral group D₄ and the permutation invariance of commutative operations. Experiments on DomainNet and a curated multi-domain negative dataset show that the proposed approach substantially outperforms similarity-based baselines and a strong zero-shot vision-language model in both plagiarism detection and transformation reconstruction. In addition to improved accuracy, the model provides a human-readable evidence trail explaining its decisions.

![Graphical abstract: the model predicts the transformation sequence relating two images; a non-empty sequence is the plagiarism decision and its visual evidence.](graphical_abstract.png)
