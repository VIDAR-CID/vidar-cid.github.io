---
title: 'Paper Reading @Summer2021: Restoration & Creation from Correspondence'
date: 2021-08-07
permalink: /posts/2021/08/paper-reading/
tags:
  - Correspondence Learning
  - Image-to-Image Translation
---

Group summer paper reading presentation on corresondence usage in image restoration and creation tasks.


## Visual Correspondence: Sparse or Dense

- Cross-view: sparse correspondence

![](/images/posts/correspondence/16495958031466.jpg)

- Adjacent frame: dense optical flow

![](/images/posts/correspondence/16495958142885.jpg)

- Cross-domain semantic correspondence

![](/images/posts/correspondence/16495958251179.jpg)

(Neural Best-buddies, Aberman et al. in ACM SIGGRAPH 2018)

## Why to incorporate additional inputs/ use correspondence

### Make the Task Easier

![](/images/posts/correspondence/16495959533428.jpg)

(Robust flash deblurring, Zhuo et al. in CVPR 2010)

![](/images/posts/correspondence/16495959652573.jpg)

(Scene Completion Using Millions of Photographs, Hays et al. in ACM SIGGRAPH 2007)

### Control the Results

![](/images/posts/correspondence/16495959948564.jpg)

(Visual Attribute Transfer through Deep Image Analogy, Liao et al. in ACM SIGGRAPH 2017)

![](/images/posts/correspondence/16495960065440.jpg)

(Cross-domain Correspondence Learning for Exemplar-based Image Translation, Zhang et al. in CVPR 2020)

### Naturally Available/Inevitable

![](/images/posts/correspondence/16495960341401.jpg)

(Across Scales & Across Dimensions: Temporal Super-Resolution using Deep Internal Learning, Zuckerman et al. in ECCV 2020)

![](/images/posts/correspondence/16495960395746.jpg)

(Light Field Super-Resolution with Zero-Shot Learning, Cheng et al. in CVPR 2021)

## How to incorporate correspondence?

![](/images/posts/correspondence/16495969370613.jpg)

- Implicit Usage(latent code)
- Explicit Usage(warp field)
- Multimodality

## Paper #1: Swapping Autoencoder for Deep Image Manipulation – NeurIPS 2020

![](/images/posts/correspondence/16495970300334.jpg)


Target: Controllable Image Manipulation
Conditional Generation needs additional prior(edge/layout)
Finding semantically meaningful latent code is non-trivial

Key idea: image swapping as a pretext task

### Approach

- Structure-texture disentangled embedding space
- Co-occurrence patch discriminator

![](/images/posts/correspondence/16495970499321.jpg)

- Style Latent code & Modulation

![](/images/posts/correspondence/16495970705304.jpg)

- Co-occurrence Patch discriminator

![](/images/posts/correspondence/16495971667609.jpg)

### Background of Modulation: How to interact between two latent space/integrate conditional signal?
![](/images/posts/correspondence/16495971094565.jpg)

Origin:

Arbitrary Style Transfer in Real-time with Adaptive Instance Normalization, Huang et al. ICCV 2017

FiLM: Visual Reasoning with a General Conditioning Layer, Perez et al. AAAI 2018

Application:

Recovering Realistic Texture in Image Super-resolution byDeep Spatial Feature Transform, Wang et al. CVPR 2018

Guided Image-to-Image Translation with Bi-Directional Feature Transformation, AlBahar and Huang, ICCV 2019

SEAN: Image Synthesis with Semantic Region-Adaptive Normalization, Zhu et al. CVPR 2020

Analyzing and Improving the Image Quality of StyleGAN, Karras et al. CVPR 2020

Adaptive Convolutions for Structure-Aware Style Transfer, Chandran et al. CVPR 2021


### Results

![](/images/posts/correspondence/16495972057514.jpg)

### Summary
- New application with an old technique
- Cooperation with other designs


## Paper #2: Adaptive Convolutions for Structure-Aware Style Transfer, Chandran et al. CVPR 2021

![](/images/posts/correspondence/16495981647384.jpg)

Target: Few-shot Synthesis(Hard to train or adapt)
Key idea: Transfer relationships/similarities

### Approach
![](/images/posts/correspondence/16495981793319.jpg)

Pairwise similarity Constraint

![](/images/posts/correspondence/16495982159180.jpg)

(1) Cross-domain consistency loss L_dist aims to preserve the relative pairwise distances between source and target generations. In this case, the relative similarities between synthesized images from z_0 and other latent codes are encouraged to be similar. (2) Relaxed realism is implemented by using two discriminators, D_img for noise sampled from the anchor region (z_anch) and D_patch otherwise.


## Takeaways

- What? Sparse vs. Dense; RGB to Semantics to Cross-Modality
- Why? Easier/Controllable/Available/Inevitable
- How? Explicit to Implicit
- Implicit Usage
- - Latent code + Modulation/Normalization
- - Constraints on “2-order” relationships
- - Weighting/Attention Mechanism and more

## More papers
StyleGAN2 Distillation for Feed-forward Image Manipulation, Viazovetskyi et al. ECCV20

Controlling Style and Semantics in Weakly-Supervised Image Generation, Pavllo  et al. ECCV 2020

COCO-FUNIT: Few-Shot Unsupervised Image Translation with a Content Conditioned Style Encoder, Saito et al. ECCV 2020

Example-Guided Image Synthesis using Masked Spatial-Channel Attention and Self-Supervision, Zheng et la. ECCV 2020

Online Exemplar Fine-Tuning for Image-to-Image Translation, Kang et al. ArXiv 2020

Swapping Autoencoder for Deep Image Manipulation, Park et al. NeurIPS 2020

Conditional Generative Modeling via Learning the Latent Space, Ramasinghe et al. ICLR 2021

Semantic Layout Manipulation with High-Resolution Sparse Attention, Zheng et al. CVPR 2021

Spatially-Invariant Style-Codes Controlled Makeup Transfer, Deng et al. CVPR 2021

Adaptive Convolutions for Structure-Aware Style Transfer, Chandran et al. CVPR 2021

ReMix: Towards Image-to-Image Translation with Limited Data, Cao et al. CVPR 2021

Learning Semantic Person Image Generation by Region-Adaptive Normalization, Lv et al. CVPR 2021
Spatially-Adaptive Pixelwise Networks for Fast Image Translation, Shaham et al. CVPR 2021

Bi-level Feature Alignment for Versatile Image Translation and Manipulation, Zhan et al. ArXiv 2021

Controllable Person Image Synthesis with Spatially-Adaptive Warped Normalization, Zhang et al. ArXiv 2021

Sketch Your Own GAN, Wang et al. ICCV 2021
