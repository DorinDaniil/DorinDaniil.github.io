---
title: "Evidential Image Matching: Predicting Transformation Sequences to Derive One Image from Another"
weight: 20
year: 2026
venue: Computer Vision and Image Understanding
status: under review
authors: "**Daniil Dorin**, Kseniia Varlamova, Andrey Grabovoy"
affiliations: "Advacheck, Tallinn; MIRAI, Moscow"
cover: cover.jpg
coverContain: true
summary: Plagiarism detection reformulated as predicting the sequence of transformations that turns one image into another. An encoder–decoder model outputs a human-readable evidence trail instead of an opaque similarity score.
tags: [image matching, plagiarism detection, encoder–decoder, VLM baseline]
links:
  - name: Code
    url: https://github.com/DorinDaniil/Image-Transform-Predict
    icon: code
---

Similarity scores are opaque and confuse visual resemblance with real derivability. This work reformulates plagiarism detection as **evidential image matching**: given a reference and a suspect image, an encoder–decoder model predicts the *sequence of transformations* (rotate, flip, crop, grayscale, blur, …) that turns one into the other. An empty sequence means "not derived".

<figure class="fig">
<div class="evidence">
  <div class="im"><img src="reference.jpg" alt="Reference image"></div>
  <span class="arrow">→</span>
  <div class="im"><img src="reference.jpg" alt="Suspect image" style="transform:rotate(90deg) scaleX(-1) scale(1.25);filter:grayscale(1) contrast(1.15)"></div>
  <span class="arrow">⇒</span>
  <div class="seq"><span class="tok">rotate_90</span><span class="tok">flip_horizontal</span><span class="tok">crop</span><span class="tok">grayscale</span><span class="tok">contrast</span></div>
</div>
<figcaption>Instead of a similarity score, the model outputs the transformation sequence that explains the suspect image.</figcaption>
</figure>

## Method

- An **encoder–decoder** maps the image pair to a token sequence from a fixed transformation vocabulary. Two encoder backbones are studied, EfficientNet-B3 and ViT-B/16, plus a contrastive Siamese baseline.
- The **Canonical Jaccard Index** is a reconstruction metric that treats equivalent sequences as equal by respecting the algebraic structure of the dihedral group D₄ and the commutativity of some operations.
- Training on DomainNet pairs, fine-tuning on a curated multi-domain negative set of look-alike but unrelated images.

## Results

The approach substantially outperforms similarity-based baselines and a strong zero-shot vision–language model in both plagiarism detection and transformation reconstruction, while producing an evidence trail that a reviewer can check by eye.
