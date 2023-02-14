---
title: "Reference-Guided Landmark Image Inpainting with Deep Feature Matching"
collection: publications
permalink: /publications/2022-07-26-TCSVT-RefMatch
date: 2022-07-26
venue: 'IEEE T-CSVT'
paperurl: ''
---


[Paper(IEEE Xplore)](https://ieeexplore.ieee.org/document/9840396)

## Abstract

Despite impressive progress made by recent image inpainting methods, they often fail to predict the original content when the corrupted region contains unique structures, especially for landmark images. Applying similar images as a reference is helpful but introduces a style gap of textures, resulting in color misalignment. To this end, we propose a style-robust approach for reference-guided landmark image inpainting, taking advantage of both the representation power of learned deep features and the structural prior from the reference image. By matching deep features, our approach builds style-robust nearest-neighbor mapping vector fields between the corrupted and reference images, in which the loss of information due to corruption leads to mismatched mapping vectors. To correct these mismatched mapping vectors based on the relationship between the uncorrupted and corrupted regions, we introduce mutual nearest neighbors as reliable anchors and interpolate around these anchors progressively. Finally, based on the corrected mapping vector fields, we propose a two-step warping strategy to complete the corrupted image, utilizing the reference image as a structural “blueprint”, avoiding the style misalignment problem. Extensive experiments show that our approach effectively and robustly assists image inpainting methods in restoring unique structures in the corrupted image.


## Method

![Framework]({{ site.baseurl }}/images/RefMatch/overview.png)


## Results

![Results]({{ site.baseurl }}/images/RefMatch/ext-nnf-vis.png)



## Acknowledegment
Thanks to Yajing Liu, Chang Chen, Shunxin Xu, Wei Huang, and Zeyu Xiao for paper revision and helpful discussions.

Special thanks to Yajing and Shunxin from Jiacheng for their consistent help and patience during Jiacheng's rookie years.
 
---

#### bibtex

```
@ARTICLE{9840396,  
author={Li, Jiacheng and Xiong, Zhiwei and Liu, Dong},  
journal={IEEE Transactions on Circuits and Systems for Video Technology},   
title={Reference-Guided Landmark Image Inpainting with Deep Feature Matching},   
year={2022},  
volume={},  
number={},  
pages={1-1},  
doi={10.1109/TCSVT.2022.3193893}}
```
