---
title: "Research Topic: Super-Resolution"
excerpt: "Super-Resolution"
author_profile: True
permalink: /low-level/sr-other.html
---

[Image](/low-level/sr-image) |
[Video](/low-level/sr-video) |
[Spectrum](/low-level/sr-spectrum) |
[Light Field](/low-level/sr-light-field) |
[Others](/low-level/sr-other)


(\*Equal contribution)


## Others (Dynamic Range / Events / Volume)

**Bidirectional Translation Between UHD-HDR and HD-SDR Videos** <br>
*Mingde Yao, Dongliang He, Xin Li, Zhihong Pan, Zhiwei Xiong* <br>
<span><pub>IEEE Transactions on Multimedia (T-MM), 2022</pub></span> <br>
[PDF](https://ieeexplore.ieee.org/abstract/document/10025794/) |
<a onclick='expandABS("yao22")'> Abstract </a>
<div style="display: none;" class=abs id="yao22"><br>
With the popularization of ultra high definition (UHD) high dynamic range (HDR) displays, recent works focus on upgrading high definition (HD) standard dynamic range (SDR) videos to UHD-HDR versions, aiming to provides richer details and higher contrasts on advanced modern displays. However, joint considering the upgrading & downgrading translations between two types of videos, which is practical in real applications, is generally neglected. On the one hand, downgrading translation is the key to showing UHD-HDR videos on HD-SDR displays. On the other hand, considering both translations enables joint optimization and results in high quality translation. To this end, we propose the bidirectional translation network (BiT-Net), which jointly considers two translations in one network for the first time. In brief, BiT-Net is elaborately designed in an invertible fashion that can be efficiently inferred along forward and backward directions for downgrading and upgrading tasks, respectively. Based on this framework, we divide each direction into three sub-tasks, i.e. , decomposition, structure-guided translation, and synthesis, to effectively translate the dynamic range and the high-frequency details. Benefiting from the dedicated architecture, our BiT-Net can work on 1) downgrading UHD-HDR videos, 2) upgrading existing HD-SDR videos, and 3) synthesizing UHD-HDR versions from the downgraded HD-SDR videos. Experiments show that the proposed method achieves state-of-the-art performances on all these three tasks.
</div>


**Towards Real-World HDRTV Reconstruction: A Data Synthesis-Based Approach** <br>
*Zhen Cheng\*, Tao Wang\*, Yong Li, Fenglong Song, Chang Chen, Zhiwei Xiong* <br>
<span><pub>European Conference on Computer Vision (ECCV), 2022</pub></span> <br>
[PDF](https://link.springer.com/chapter/10.1007/978-3-031-19800-7_12) |
[Dataset](https://github.com/huawei-noah/benchmark/tree/main/RealHDRTV_dataset) |
<a onclick='expandABS("cheng22")'> Abstract </a>
<div style="display: none;" class=abs id="cheng22"><br>
Existing deep learning based HDRTV reconstruction methods assume one kind of tone mapping operators (TMOs) as the degradation procedure to synthesize SDRTV-HDRTV pairs for supervised training. In this paper, we argue that, although traditional TMOs exploit efficient dynamic range compression priors, they have several drawbacks on modeling the realistic degradation: information over-preservation, color bias and possible artifacts, making the trained reconstruction networks hard to generalize well to real-world cases. To solve this problem, we propose a learning-based data synthesis approach to learn the properties of real-world SDRTVs by integrating several tone mapping priors into both network structures and loss functions. In specific, we design a conditioned two-stream network with prior tone mapping results as a guidance to synthesize SDRTVs by both global and local transformations. To train the data synthesis network, we form a novel self-supervised content loss to constraint different aspects of the synthesized SDRTVs at regions with different brightness distributions and an adversarial loss to emphasize the details to be more realistic. To validate the effectiveness of our approach, we synthesize SDRTV-HDRTV pairs with our method and use them to train several HDRTV reconstruction networks. Then we collect two inference datasets containing both labeled and unlabeled real-world SDRTVs, respectively. Experimental results demonstrate that, the networks trained with our synthesized data generalize significantly better to these two real-world datasets than existing solutions.
</div>



**Boosting Event Stream Super-Resolution with a Recurrent Neural Network** <br>
*Wenming Weng, Yueyi Zhang, Zhiwei Xiong* <br>
<span><pub>European Conference on Computer Vision (ECCV), 2022</pub></span> <br>
[PDF](https://link.springer.com/chapter/10.1007/978-3-031-20068-7_27) |
<a onclick='expandABS("weng22")'> Abstract </a>
<div style="display: none;" class=abs id="weng22"><br>
Existing methods for event stream super-resolution (SR) either require high-quality and high-resolution frames or underperform for large factor SR. To address these problems, we propose a recurrent neural network for event SR without frames. First, we design a temporal propagation net for incorporating neighboring and long-range event-aware contexts that facilitates event SR. Second, we build a spatiotemporal fusion net for reliably aggregating the spatiotemporal clues of event stream. These two elaborate components are tightly synergized for achieving satisfying event SR results even for 16×
 SR. Synthetic and real-world experimental results demonstrate the clear superiority of our method. Furthermore, we evaluate our method on two downstream event-driven applications, i.e., object recognition and video reconstruction, achieving remarkable performance boost over existing methods.
 </div>


**Isotropic Reconstruction of 3D EM Images with Unsupervised Degradation Learning** <br>
*Shiyu Deng, Xueyang Fu, Zhiwei Xiong, Chang Chen, Dong Liu, Xuejin Chen, Qing Ling, Feng Wu* <br>
<span><pub>International Conference on Medical Image Computing and Computer Assisted Intervention (MICCAI), 2020</pub></span> <br> 
[PDF](https://link.springer.com/chapter/10.1007/978-3-030-59722-1_16) |
<a onclick='expandABS("deng20")'> Abstract </a>
<div style="display: none;" class=abs id="deng20"><br>
The isotropic reconstruction of 3D electron microscopy (EM) images with low axial resolution is of great importance for biological analysis. Existing deep learning-based methods rely on handcrafted down-scaled training data, which does not model the real degradation accurately and thus leads to unsatisfying performance in practice. To address this problem, we propose a universal and unsupervised framework to simultaneously learn the real axial degradation and the isotropic reconstruction of 3D EM images. First, we train a degradation network using unpaired low-resolution (LR) and high-resolution (HR) slices, both of which are from real data, in an adversarial manner. Then, the degradation network is further used to generate realistic LR data from HR labels to form paired training data. In this way, the generated degraded data is consistent with the real axial degradation process, which guarantees the generalization ability of subsequent reconstruction networks to the real data. Our framework has the flexibility to work with different existing reconstruction methods. Experiments on both simulated and real anisotropic EM images validate the superiority of our framework.
</div>
