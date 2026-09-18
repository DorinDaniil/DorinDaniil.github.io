---
title: "Garage: generative augmentation framework"
weight: 30
year: 2024
stars: 13
cover: abstract.jpg
summary: Replaces objects in images with newly generated ones. Grounded-SAM finds and masks the object, an Augmenter model proposes replacements and prompts, PowerPaint inpaints the result.
tags: [generative models, augmentation, diffusion]
links:
  - name: GitHub
    url: https://github.com/DorinDaniil/Garage
    icon: github
---

Classical augmentation changes pixels; Garage changes *content*. Given an image and a target object, it produces new training samples where that object is swapped for a plausible alternative, keeping the scene intact.

![Garage pipeline: detect and segment the object, propose a replacement and prompt, inpaint.](abstract.jpg)

## Pipeline

1. **Grounding DINO + Segment Anything** locate the object from a text query and produce a mask.
2. The **Augmenter** model generates candidate replacement objects and prompts.
3. **PowerPaint** inpaints the masked region with the new object.

A Gradio demo lets you try it in the browser; the repository includes depth-conditioned examples and scripts to download the required checkpoints.
