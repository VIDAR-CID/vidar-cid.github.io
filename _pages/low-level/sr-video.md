---
title: "Research Topic: Super-Resolution"
excerpt: "Super-Resolution"
author_profile: True
permalink: /low-level/sr-video.html
---

[Image](/low-level/sr-image) |
[Video](/low-level/sr-video) |
[Spectrum](/low-level/sr-spectrum) |
[Light Field](/low-level/sr-light-field) |
[Others](/low-level/sr-other)

(\*Equal contribution)


## Video

**Propagating Difference Flows for Efficient Video Super-Resolution** <br>
*Ruisheng Gao, Zeyu Xiao, Zhiwei Xiong* <br>
<span><pub>British Machine Vision Conference (BMVC), 2022</pub></span> <br>
[PDF](https://bmvc2022.mpi-inf.mpg.de/0060.pdf) |
<a onclick='expandABS("gao22")'> Abstract </a>
<div style="display: none;" class=abs id="gao22"><br>
Recent years have witnessed the advancement of video super-resolution (VSR) with elaborately-designed multi-frame alignment and space-time fusion/refinement techniques. However, both techniques require heavy computational burden and memory consumption, hindering existing VSR networks from being deployed on resource-constrained platforms (e.g., smartphones and wearable devices). In this paper, we propose an efficient and lightweight VSR network with two special designs. First, we propose a novelmotion propagation scheme which propagates difference flowsfor efficient feature alignment. The difference flow is sparse and computational-friendly which focuses on texture details. After estimating the preliminary difference flow with an initial motion estimator, we then design an adaptive motion modification module for frame-pair wise adaptation through bidirectional propagation. Second, a dense feature distillation module is designed for further refining the aligned features efficiently. Thanks to both designs, ournetwork achieves comparable performance with state-of-the-art VSR methods while enjoying a clear advantage in model size and computational efficiency
</div>

**EVA$^{2}$: Event-Assisted Video Frame Interpolation via Cross-Modal Alignment and Aggregation** <br>
*Zeyu Xiao, Wenming Weng, Yueyi Zhang, Zhiwei Xiong* <br>
<span><pub>IEEE Transactions on Computational Imaging (T-CI), 2022</pub></span> <br>
[PDF](https://ieeexplore.ieee.org/document/9982428/) |
<a onclick='expandABS("xiao22")'> Abstract </a>
<div style="display: none;" class=abs id="xiao22"><br>
We consider the problem of event-assisted video frame interpolation (VFI), a new track for VFI, by introducing the event data, a novel sensing modality, into the process of generating intermediate frames from low-frame-rate videos. This new track challenges existing methods in two aspects: (1) how to utilize the event data to align boundary keyframes to intermediate ones, especially when there are corruptions in scenes ( e.g. , non-uniform motion, object occlusions, and illumination changes); (2) how to effectively utilize and aggregate cross-modal information for further mitigating corruptions and refining details. In this paper, we propose a novel E vent-assisted V FI method with cross-modal A lignment and A ggregation, termed EVA2 , to address these challenges. First, to handle corruptions during alignment, we devise the cross-modal Event-Guided Alignment (EGA) module, in which the intermediate frames are aligned at both the feature and the image levels. The alignment operation in the EGA module is guided by the offset maps generated from the event data and information extracted from the input boundary keyframes. Second, we propose the cross-modal Event-aware Dynamic Aggregation (EDA) module, in which the event-aware dynamic convolution operation is applied to aggregate the event data with the aligned results adaptively for further improvements. Extensive experiments on both synthetic and real-world datasets validate the effectiveness of our EVA2 .
</div>


**Space-Time Distillation for Video Super-Resolution** <br>
*Zeyu Xiao, Xueyang Fu, Jie Huang, Zhen Cheng, Zhiwei Xiong* <br>
<span><pub>IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 2021</pub></span> <br> 
[PDF](https://openaccess.thecvf.com/content/CVPR2021/html/Xiao_Space-Time_Distillation_for_Video_Super-Resolution_CVPR_2021_paper) |
<a onclick='expandABS("xiao21")'> Abstract </a>
<div style="display: none;" class=abs id="xiao21"><br>
Compact video super-resolution (VSR) networks can be easily deployed on resource-limited devices, e.g., smart-phones and wearable devices, but have considerable performance gaps compared with complicated VSR networks that require a large amount of computing resources. In this paper, we aim to improve the performance of compact VSR networks without changing their original architectures, through a knowledge distillation approach that transfers knowledge from a complicated VSR network to a compact one. Specifically, we propose a space-time distillation (STD) scheme to exploit both spatial and temporal knowledge in the VSR task. For space distillation, we extract spatial attention maps that hints the high-frequency video content from both networks, which are further used for transferring spatial modeling ability. For time distillation, we narrow the performance gap between compact models and complicated models by distilling the feature similarity of the temporal memory cells, which is encoded from the sequence of feature maps generated in the training clips using ConvLSTM. During the training process, STD can be easily incorporated into any network without changing the original network architecture. Experimental results on standard benchmarks demonstrate that, in resource-constrained situations, the proposed method notably improve the performance of existing VSR networks without increasing the inference time.
</div>



**Stereo Video Super-Resolution via Exploiting View-Temporal Correlation** <br>
*Ruikang Xu, Zeyu Xiao, Mingde Yao, Yueyi Zhang, Zhiwei Xiong* <br>
<span><pub>ACM International Conference on Multimedia (MM), 2021</pub></span> <br>
[PDF](https://dl.acm.org/doi/10.1145/3474085.3475189) |
<a onclick='expandABS("xu21")'> Abstract </a>
<div style="display: none;" class=abs id="xu21"><br>
Stereo Video Super-Resolution (StereoVSR) aims to generate high-resolution video steams from two low-resolution videos under stereo settings. Existing video super-resolution and stereo image super-resolution techniques can be extended to tackle the StereoVSR task, yet they cannot make full use of the multi-view and temporal information to achieve satisfactory performance. In this paper, we propose a novel Stereo Video Super-Resolution Network (SVSRNet) to fulfill the StereoVSR task via exploiting view-temporal correlations. First, we devise a view-temporal attention module (VTAM) to integrate the information of cross-time-cross-view for constructing high-resolution stereo videos. Second, we propose a spatial-temporal fusion module (STFM), which aggregates the information across time in intra-view to emphasize important features for subsequent restoration. In addition, we design a view-temporal consistency loss function to enforce consistency constraint of superresolved stereo videos. Comprehensive experimental results demonstrate that our method generates superior results.
</div>



**Space-Time Video Super-Resolution Using Temporal Profiles** <br>
*Zeyu Xiao, Zhiwei Xiong, Xueyang Fu, Dong Liu, Zheng-Jun Zha* <br>
<span><pub>ACM International Conference on Multimedia (MM), 2020</pub></span> <br>
[PDF](https://dl.acm.org/doi/10.1145/3394171.3413667) |
<a onclick='expandABS("xiao20")'> Abstract </a>
<div style="display: none;" class=abs id="xiao20"><br>
In this paper, we propose a novel space-time video super-resolution method, which aims to recover a high-frame-rate and high-resolution video from its low-frame-rate and low-resolution observation. Existing solutions seldom consider the spatial-temporal correlation and the long-term temporal context simultaneously and thus are limited in the restoration performance. Inspired by the epipolar-plane image used in multi-view computer vision tasks, we first propose the concept of temporal-profile super-resolution to directly exploit the spatial-temporal correlation in the long-term temporal context. Then, we specifically design a feature shuffling module for spatial retargeting and spatial-temporal information fusion, which is followed by a refining module for artifacts alleviation and detail enhancement. Different from existing solutions, our method does not require any explicit or implicit motion estimation, making it lightweight and flexible to handle any number of input frames. Comprehensive experimental results demonstrate that our method not only generates superior space-time video super-resolution results but also retains competitive implementation efficiency.
</div>



**Two-Stream Action Recognition-Oriented Video Super-Resolution** <br>
*Haochen Zhang, Dong Liu, Zhiwei Xiong* <br>
<span><pub>International Conference on Computer Vision (ICCV), 2019</pub></span> <br>
[PDF](http://openaccess.thecvf.com/content_ICCV_2019/papers/Zhang_Two-Stream_Action_Recognition-Oriented_Video_Super-Resolution_ICCV_2019_paper.pdf) |
<a onclick='expandABS("zhang19")'> Abstract </a>
<div style="display: none;" class=abs id="zhang19"><br>
We study the video super-resolution (SR) problem for facilitating video analytics tasks, e.g. action recognition, instead of for visual quality. The popular action recognition methods based on convolutional networks, exemplified by two-stream networks, are not directly applicable on video of low spatial resolution. This can be remedied by performing video SR prior to recognition, which motivates us to improve the SR procedure for recognition accuracy. Tailored for two-stream action recognition networks, we propose two video SR methods for the spatial and temporal streams respectively. On the one hand, we observe that regions with action are more important to recognition, and we propose an optical-flow guided weighted mean-squared-error loss for our spatial-oriented SR (SoSR) network to emphasize the reconstruction of moving objects. On the other hand, we observe that existing video SR methods incur temporal discontinuity between frames, which also worsens the recognition accuracy, and we propose a siamese network for our temporal-oriented SR (ToSR) training that emphasizes the temporal continuity between consecutive frames. We perform experiments using two state-of-the-art action recognition networks and two well-known datasets--UCF101 and HMDB51. Results demonstrate the effectiveness of our proposed SoSR and ToSR in improving recognition accuracy.
</div>


