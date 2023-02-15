---
title: "Research Topic: Super-Resolution"
excerpt: "Super-Resolution"
author_profile: True
permalink: /low-level/sr-spectrum.html
---


[Image](/low-level/sr-image) |
[Video](/low-level/sr-video) |
[Spectrum](/low-level/sr-spectrum) |
[Light Field](/low-level/sr-light-field) |
[Others](/low-level/sr-other)


(\*Equal contribution)

## Spectrum

**Continuous Spectral Reconstruction from RGB Images via Implicit Neural Representation** <br>
*Ruikang Xu, Mingde Yao, Chang Chen, Lizhi Wang, Zhiwei Xiong* <br>
<span><pub>European Conference on Computer Vision Workshops (ECCVW), 2022</pub></span> <br>
<span><highlighted>MIPI best paper honorable mention</highlighted><span> |
[PDF](https://arxiv.org/abs/2112.13003) |
<a onclick='expandABS("xu22")'> Abstract </a>
<div style="display: none;" class=abs id="xu22"><br>
Existing methods for spectral reconstruction usually learn a discrete mapping from RGB images to a number of spectral bands. However, this modeling strategy ignores the continuous nature of spectral signature. In this paper, we propose Neural Spectral Reconstruction (NeSR) to lift this limitation, by introducing a novel continuous spectral representation. To this end, we embrace the concept of implicit function and implement a parameterized embodiment with a neural network. Specifically, we first adopt a backbone network to extract spatial features of RGB inputs. Based on it, we devise Spectral Profile Interpolation (SPI) module and Neural Attention Mapping (NAM) module to enrich deep features, where the spatial-spectral correlation is involved for a better representation. Then, we view the number of sampled spectral bands as the coordinate of continuous implicit function, so as to learn the projection from deep features to spectral intensities. Extensive experiments demonstrate the distinct advantage of NeSR in reconstruction accuracy over baseline methods. Moreover, NeSR extends the flexibility of spectral reconstruction by enabling an arbitrary number of spectral bands as the target output.
</div>


**Deep Residual Attention Network for Spectral Image Super-Resolution** <br>
*Zhan Shi, Chang Chen, Zhiwei Xiong, Dong Liu, Zheng-Jun Zha, Feng Wu* <br>
<span><pub>European Conference on Computer Vision Workshops (ECCVW), 2018</pub></span> <br>
<span><highlighted>PIRM winner</highlighted><span> |
[PDF](https://link.springer.com/chapter/10.1007/978-3-030-11021-5_14) |
[Code](https://github.com/contstriver/DRAN) |
<a onclick='expandABS("shi18eccv")'> Abstract </a>
<div style="display: none;" class=abs id="shi18eccv"><br>
Spectral imaging sensors often suffer from low spatial resolution, as there exists an essential tradeoff between the spectral and spatial resolutions that can be simultaneously achieved, especially when the temporal resolution needs to be retained. In this paper, we propose a novel deep residual attention network for the spatial super-resolution (SR) of spectral images. The proposed method extends the classic residual network by 1) directly using the 3D low-resolution (LR) spectral image as input instead of upsampling the 2D bandwise images separately, and 2) integrating the channel attention mechanism into the residual network. These two operations fully exploit the correlations across both the spectral and spatial dimensions and greatly promote the performance of spectral image SR. In addition, for the scenario when stereo pairs of LR spectral and high-resolution (HR) RGB measurements are available, we design a fusion framework based on the proposed network. The spatial resolution of the spectral input is enhanced in one branch, while the spectral resolution of the RGB input is enhanced in the other. These two branches are then fused together through the attention mechanism again to reconstruct the final HR spectral image, which achieves further improvement compared to using the single LR spectral input. Experimental results demonstrate the superiority of the proposed method over plain residual networks, and our method is one of the winning solutions in the PIRM 2018 Spectral Super-resolution Challenge.
</div>


**HSCNN+: Advanced CNN-Based Hyperspectral Recovery From RGB Images** <br>
*Zhan Shi, Chang Chen, Zhiwei Xiong, Dong Liu, Feng Wu* <br>
<span><pub>IEEE/CVF Conference on Computer Vision and Pattern Recognition Workshops (CVPRW), 2018</pub></span> <br> 
<span><highlighted>NTIRE winner</highlighted><span> |
[PDF](http://openaccess.thecvf.com/content_cvpr_2018_workshops/w13/html/Shi_HSCNN_Advanced_CNN-Based_CVPR_2018_paper) |
[Code](https://github.com/ngchc/HSCNN-Plus) |
<a onclick='expandABS("shi18cvpr")'> Abstract </a>
<div style="display: none;" class=abs id="shi18cvpr"><br>
Hyperspectral recovery from a single RGB image has seen a great improvement with the development of deep convolutional neural networks (CNNs). In this paper, we propose two advanced CNNs for the hyperspectral reconstruction task, collectively called HSCNN+. We first develop a deep residual network named HSCNN-R, which comprises a number of residual blocks. The superior performance of this model comes from the modern architecture and optimization by removing the hand-crafted upsampling in HSCNN. Based on the promising results of HSCNN-R, we propose another distinct architecture that replaces the residual block by the dense block with a novel fusion scheme, leading to a new network named HSCNN-D. This model substantially deepens the network structure for a more accurate solution. Experimental results demonstrate that our proposed models significantly advance the state-of-the-art. In the NTIRE 2018 Spectral Reconstruction Challenge, our entries rank the 1st (HSCNN-D) and 2nd (HSCNN-R) places on both the "Clean" and "Real World" tracks.
</div>


**HSCNN: CNN-Based Hyperspectral Image Recovery from Spectrally Undersampled Projections** <br>
*Zhiwei Xiong, Zhan Shi, Huiqun Li, Lizhi Wang, Dong Liu, Feng Wu* <br>
<span><pub>International Conference on Computer Vision Workshops (ICCVW), 2017</pub></span> <br>
[PDF](http://openaccess.thecvf.com/content_ICCV_2017_workshops/w9/html/Xiong_HSCNN_CNN-Based_Hyperspectral_ICCV_2017_paper) |
<a onclick='expandABS("xiong17")'> Abstract </a>
<div style="display: none;" class=abs id="xiong17"><br>
This paper presents a unified deep learning framework to recover hyperspectral images from spectrally undersampled projections. Specifically, we investigate two kinds of representative projections, RGB and compressive sensing (CS) measurements. These measurements are first upsampled in the spectral dimension through simple interpolation or CS reconstruction, and the proposed method learns an end-to-end mapping from a large number of upsampled/groundtruth hyperspectral image pairs. The mapping is represented as a deep convolutional neural network (CNN) that takes the spectrally upsampled image as input and outputs the enhanced hyperspetral one. We explore different network configurations to achieve high reconstruction fidelity. Experimental results on a variety of test images demonstrate significantly improved performance of the proposed method over the state-of-the-arts.
</div>
