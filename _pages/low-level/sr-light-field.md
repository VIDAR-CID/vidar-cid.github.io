---
title: "Research Topic: Super-Resolution"
excerpt: "Super-Resolution"
author_profile: True
permalink: /low-level/sr-light-field.html
---

[Image](/low-level/sr-image) |
[Video](/low-level/sr-video) |
[Spectrum](/low-level/sr-spectrum) |
[Light Field](/low-level/sr-light-field) |
[Others](/low-level/sr-other)

(\*Equal contribution)



## Light Field

**Spatial-Angular Versatile Convolution for Light Field Reconstruction** <br>
*Zhen Cheng, Yutong Liu, Zhiwei Xiong* <br>
<span><pub>IEEE Transactions on Computational Imaging (T-CI), 2022</pub></span> <br>
[PDF](https://ieeexplore.ieee.org/document/9966657/) |
<a onclick='expandABS("cheng22")'> Abstract </a>
<div style="display: none;" class=abs id="cheng22"><br>
Spatial-angular separable convolution (SAS-conv) has been widely used for efficient and effective 4D light field (LF) feature embedding in different tasks, which mimics a 4D convolution by alternatively operating on 2D spatial slices and 2D angular slices. In this paper, we argue that, despite its global intensity modeling capabilities, SAS-conv can only embed local geometry information into the features, resulting in inferior performances in the regions with textures and occlusions. Because the epipolar lines are highly related to the scene depth, we introduce the concept of spatial-angular correlated convolution (SAC-conv). By alternating 2D convolutions on the vertical and horizontal epipolar slices, SAC-conv can embed global and robust geometry information into the features. We verify that SAS-conv and SAC-conv are skilled at different aspects of 4D LF feature embedding through a detailed feature and error analysis. Based on their complementarity, we further combine SAS-conv and SAC-conv by a parallel residual connection, forming a new spatial-angular versatile convolution (SAV-conv) module. We conduct comprehensive experiments on two representative LF reconstruction tasks, i.e., LF angular super-resolution and LF spatial super-resolution. Both the quantitative and qualitative results demonstrate that, without any extra parameters, networks upgraded with our proposed SAV-conv notably outperform those upgraded with SAS-conv and achieve a new state-of-the-art performance.
</div>


**Light Field Super-Resolution With Zero-Shot Learning** <br>
*Zhen Cheng, Zhiwei Xiong, Chang Chen, Dong Liu, Zheng-Jun Zha* <br>
<span><pub>IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 2021</pub></span> <br>
<span><highlighted>Oral</highlighted><span> |
[PDF](https://openaccess.thecvf.com/content/CVPR2021/html/Cheng_Light_Field_Super-Resolution_With_Zero-Shot_Learning_CVPR_2021_paper) |
[Code](https://github.com/Joechann0831/LFZSSR) |
<a onclick='expandABS("cheng21")'> Abstract </a>
<div style="display: none;" class=abs id="cheng21"><br>
Deep learning provides a new avenue for light field super-resolution (SR). However, the domain gap caused by drastically different light field acquisition conditions poses a main obstacle in practice. To fill this gap, we propose a zero-shot learning framework for light field SR, which learns a mapping to super-resolve the reference view with examples extracted solely from the input low-resolution light field itself. Given highly limited training data under the zero-shot setting, however, we observe that it is difficult to train an end-to-end network successfully. Instead, we divide this challenging task into three sub-tasks, i.e., pre-upsampling, view alignment, and multi-view aggregation, and then conquer them separately with simple yet efficient CNNs. Moreover, the proposed framework can be readily extended to finetune the pre-trained model on a source dataset to better adapt to the target input, which further boosts the performance of light field SR in the wild. Experimental results validate that our method not only outperforms classic non-learning-based methods, but also generalizes better to unseen light fields than state-of-the-art deep-learning-based methods when the domain gap is large.
</div>


**Light Field Super-Resolution By Jointly Exploiting Internal and External Similarities** <br>
*Zhen Cheng, Zhiwei Xiong, Dong Liu* <br>
<span><pub>IEEE Transactions on Circuits and Systems for Video Technology (T-CSVT), 2020</pub></span> <br>
[PDF](https://ieeexplore.ieee.org/document/8733069) |
[Code](https://github.com/Joechann0831/LFSR-FusNet) |
<a onclick='expandABS("cheng20")'> Abstract </a>
<div style="display: none;" class=abs id="cheng20"><br>
Light field images taken by plenoptic cameras often have a tradeoff between spatial and angular resolutions. In this paper, we propose a novel spatial super-resolution approach for light field images by jointly exploiting internal and external similarities. The internal similarity refers to the correlations across the angular dimensions of the 4D light field itself, while the external similarity refers to the cross-scale correlations learned from an external light field dataset. Specifically, we advance the classic projection-based method that exploits the internal similarity by introducing the intensity consistency checking criterion and a back-projection refinement, while the external correlation is learned by a CNN-based method which aggregates all warped high-resolution sub-aperture images upsampled from the low-resolution input using a single image super-resolution method. By analyzing the error distributions of the above two methods and investigating the upperbound of combining them, we find that the internal and external similarities are complementary to each other. Accordingly, we further propose a pixel-wise adaptive fusion network to take advantage of both their merits by learning a weighting matrix. Experimental results on both synthetic and real-world light field datasets validate the superior performance of the proposed approach over the state-of-the-arts.
</div>



**Light Field Super-Resolution: A Benchmark** <br>
*Zhen Cheng, Zhiwei Xiong, Chang Chen, Dong Liu* <br>
<span><pub>IEEE/CVF Conference on Computer Vision and Pattern Recognition Workshops (CVPRW), 2018</pub></span> <br> 
[PDF](http://openaccess.thecvf.com/content_CVPRW_2019/html/NTIRE/Cheng_Light_Field_Super-Resolution_A_Benchmark_CVPRW_2019_paper) |
[Code](https://github.com/Joechann0831/LFSRBenchmark) |
<a onclick='expandABS("cheng18")'> Abstract </a>
<div style="display: none;" class=abs id="cheng18"><br>
Lenslet-based light field imaging generally suffers from a fundamental trade-off between spatial and angular resolutions, which limits its promotion to practical applications. To this end, a substantial amount of efforts have been dedicated to light field super-resolution (SR) in recent years. Despite the demonstrated success, existing light field SR methods are often evaluated based on different degradation assumptions using different datasets, and even contradictory results are reported in literature. In this paper, we conduct the first systematic benchmark evaluation for representative light field SR methods on both synthetic and real-world datasets with various downsampling kernels and scaling factors. We then analyze and discuss the advantages and limitations of each kind of method from different perspectives. Especially, we find that CNN-based single image SR without using any angular information outperforms most light field SR methods even including learning-based ones. This benchmark evaluation, along with the comprehensive analysis and discussion, sheds light on the future researches in light field SR.
</div>


