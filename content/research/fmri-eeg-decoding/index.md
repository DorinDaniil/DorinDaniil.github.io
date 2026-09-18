---
title: "Decoding Visual Information from Neural Signals: Image Reconstruction Based on Joint fMRI and EEG Analysis"
weight: 10
year: 2025
venue: Informatics and its Applications
authors: "**Daniil Dorin**, Nikita Kiselev, Andrey Grabovoy"
cover: scheme.png
coverContain: true
summary: A multimodal architecture that jointly processes fMRI and EEG signals to reconstruct visual stimuli, with contrastive alignment to CLIP and a two-stage diffusion generation pipeline.
tags: [fMRI, EEG, contrastive learning, diffusion models]
links:
  - name: Paper
    url: https://doi.org/10.14357/19922264260203
    icon: paper
bibtex: |
  @article{dorin2025decoding,
    title   = {Decoding visual information from neural signals: image reconstruction based on joint functional magnetic resonance imaging and electroencephalography analysis},
    author  = {Dorin, Daniil D. and Kiselev, Nikita and Grabovoy, Andrey V.},
    journal = {Informatika i ee Primeneniya},
    volume  = {20},
    number  = {2},
    pages   = {35--49},
    doi     = {10.14357/19922264260203}
  }
---

Reconstructing visual stimuli from neural signals is a fundamental challenge in neurodecoding, lying at the intersection of computational neuroscience and modern machine learning. Despite recent advances achieved using contrastive representations and diffusion-based generative models, most existing approaches are limited to a single neuroimaging modality — either functional magnetic resonance imaging (fMRI) with high spatial resolution, or electroencephalography (EEG) with high temporal resolution. The integration of both modalities remains a largely unexplored area. In this work, a multimodal architecture is proposed that jointly processes fMRI and EEG signals to reconstruct visual stimuli. Brain activity embeddings are trained contrastively to align with CLIP image embeddings. The proposed two-stage generation pipeline comprises synthesis of an intermediate latent representation via a prior model trained on joint fMRI–EEG vectors, followed by decoding this representation using a pretrained diffusion model conditioned on CLIP embeddings. Experiments on a publicly available multimodal dataset demonstrate the efficacy of the proposed architecture for neural decoding. Quantitatively, the multimodal model surpasses unimodal baselines in terms of CLIP-Score, underscoring the importance of jointly leveraging fMRI and EEG signals for accurate visual stimulus reconstruction.

![Proposed architecture: contrastive alignment of combined fMRI–EEG embeddings with CLIP features, and the two-stage generation pipeline.](scheme.png)

![Reconstructions of test stimuli. Rows: original frame; reference reconstruction; proposed method; proposed method with diffusion prior.](reconstructions.jpg)
