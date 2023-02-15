---
title: "Research Topic: Super-Resolution"
excerpt: "Super-Resolution"
author_profile: True
permalink: /low-level/sr-image.html
---

[Image](/low-level/sr-image) |
[Video](/low-level/sr-video) |
[Spectrum](/low-level/sr-spectrum) |
[Light Field](/low-level/sr-light-field) |
[Others](/low-level/sr-other)


(\*Equal contribution)

<!-- ![SemIA]({{ site.baseurl }}/images/SemIA/teaser.png) -->
## Image

**MuLUT: Cooperating Multiple Look-Up Tables for Efficient Super-Resolution** <br>
*Jiacheng Li\*, Chang Chen\*, Zhen Cheng, Zhiwei Xiong* <br>
<span><pub>European Conference on Computer Vision (ECCV), 2022</pub></span> <br>
[Project](https://mulut.pages.dev) |
[PDF](https://link.springer.com/chapter/10.1007/978-3-031-19797-0_14) |
[Code](https://github.com/ddlee-cn/MuLUT) | 
<a onclick='expandABS("li22")'> Abstract </a>
<div style="display: none;" class=abs id="li22"><br>
The high-resolution screen of edge devices stimulates a strong demand for efficient image super-resolution (SR). An emerging research, SR-LUT, responds to this demand by marrying the look-up table (LUT) with learning-based SR methods. However, the size of a single LUT grows exponentially with the increase of its indexing capacity. Consequently, the receptive field of a single LUT is restricted, resulting in inferior performance. To address this issue, we extend SR-LUT by enabling the cooperation of Multiple LUTs, termed MuLUT. Firstly, we devise two novel complementary indexing patterns and construct multiple LUTs in parallel. Secondly, we propose a re-indexing mechanism to enable the hierarchical indexing between multiple LUTs. In these two ways, the total size of MuLUT is linear to its indexing capacity, yielding a practical method to obtain superior performance. We examine the advantage of MuLUT on five SR benchmarks. MuLUT achieves a significant improvement over SR-LUT, up to 1.1 dB PSNR, while preserving its efficiency. Moreover, we extend MuLUT to address demosaicing of Bayer-patterned images, surpassing SR-LUT on two benchmarks by a large margin.
</div>


**Camera Lens Super-Resolution** <br>
*Chang Chen, Zhiwei Xiong, Xinmei Tian, Zheng-Jun Zha, Feng Wu* <br>
<span><pub>IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR), 2019</pub></span> <br>
[PDF](http://openaccess.thecvf.com/content_CVPR_2019/html/Chen_Camera_Lens_Super-Resolution_CVPR_2019_paper) |
[Code](https://github.com/ngchc/CameraSR) |
<a onclick='expandABS("chen19")'> Abstract </a>
<div style="display: none;" class=abs id="chen19"><br>
Existing methods for single image super-resolution (SR) are typically evaluated with synthetic degradation models such as bicubic or Gaussian downsampling. In this paper, we investigate SR from the perspective of camera lenses, named as CameraSR, which aims to alleviate the intrinsic tradeoff between resolution (R) and field-of-view (V) in realistic imaging systems. Specifically, we view the R-V degradation as a latent model in the SR process and learn to reverse it with realistic low- and high-resolution image pairs. To obtain the paired images, we propose two novel data acquisition strategies for two representative imaging systems (i.e., DSLR and smartphone cameras), respectively. Based on the obtained City100 dataset, we quantitatively analyze the performance of commonly-used synthetic degradation models, and demonstrate the superiority of CameraSR as a practical solution to boost the performance of existing SR methods. Moreover, CameraSR can be readily generalized to different content and devices, which serves as an advanced digital zoom tool in realistic imaging systems.
</div>


**UDNet: Up-Down Network for Compact and Efficient Feature Representation in Image Super-Resolution** <br>
*Chang Chen, Xinmei Tian, Feng Wu, Zhiwei Xiong* <br>
<span><pub>International Conference on Computer Vision Workshops (ICCVW), 2017</pub></span> <br> 
[PDF](https://ieeexplore.ieee.org/document/8265339) |
<a onclick='expandABS("chen17")'> Abstract </a>
<div style="display: none;" class=abs id="chen17"><br>
Recently, image super-resolution (SR) using convolutional neural networks (CNNs) have achieved remarkable performance. However, there is a tradeoff between performance and speed of SR, depending on whether feature representation and learning are conducted in high-resolution (HR) or low-resolution (LR) space. Generally, to pursue real-time SR, the number of parameters in CNNs has to be restricted, which results in performance degradation. In this paper, we propose a compact and efficient feature representation for real-time SR, named up-down network (UDNet). Specifically, a novel hourglass-shape structure is introduced by combining transposed convolution and spatial aggregation. This structure enables the network to transfer the feature representations between LR and HR spaces multiple times to learn a better mapping. Comprehensive experiments demonstrate that, compared with existing CNN models, UDNet achieves real-time SR without performance degradation on widely used benchmarks.
</div>


**Example-Based Super-Resolution With Soft Information and Decision** <br>
*Zhiwei Xiong, Dong Xu, Xiaoyan Sun, Feng Wu* <br>
<span><pub>IEEE Transactions on Multimedia (T-MM), 2013</pub></span> <br>
[PDF](http://ieeexplore.ieee.org/document/6518133/) |
<a onclick='expandABS("xiong13")'> Abstract </a>
<div style="display: none;" class=abs id="xiong13"><br>
The one-to-one correspondence between co-occurrence image patches of two different resolutions is extensively used in example-based super-resolution (SR). Due to the dimensionality gap between low resolution (LR) and high resolution (HR) spaces, however, an LR patch may correspond to a number of HR patches in practice. This ambiguity is difficult to be overcome with examples representing a deterministic mapping. In this paper, we propose a statistical method for exploiting the one-to-many correspondence between LR and HR patches, which we call soft information and decision. Soft information means an LR patch is mapped to a pixel-wise distribution of all its possible HR counterparts, rather than a single or a limited set of HR candidates. Relying on the soft information, example-based SR is then regarded as an optimization problem to best preserve the local consistency in the recovered HR image. This problem is solved with an efficient message passing algorithm with a factor graph model. The final decision on the HR pixel value is made upon the maximum a posteriori estimation and is called a soft decision. Experimental results demonstrate the superiority of the proposed method compared with the state-of-the-art methods, in terms of both the subjective and objective quality of synthesized HR images.
</div>


**Robust Web Image/Video Super-Resolution** <br>
*Zhiwei Xiong, Xiaoyan Sun, Feng Wu* <br>
<span><pub>IEEE Transactions on Image Processing (T-IP), 2010</pub></span> <br>
[PDF](https://ieeexplore.ieee.org/abstract/document/5430911/) |
<a onclick='expandABS("xiong10")'> Abstract </a>
<div style="display: none;" class=abs id="xiong10"><br>
This paper proposes a robust single-image super-resolution method for enlarging low quality web image/video degraded by downsampling and compression. To simultaneously improve the resolution and perceptual quality of such web image/video, we bring forward a practical solution which combines adaptive regularization and learning-based super-resolution. The contribution of this work is twofold. First, we propose to analyze the image energy change characteristics during the iterative regularization process, i.e., the energy change ratio between primitive (e.g., edges, ridges and corners) and nonprimitive fields. Based on the revealed convergence property of the energy change ratio, appropriate regularization strength can then be determined to well balance compression artifacts removal and primitive components preservation. Second, we verify that this adaptive regularization can steadily and greatly improve the pair matching accuracy in learning-based super-resolution. Consequently, their combination effectively eliminates the quantization noise and meanwhile faithfully compensates the missing high-frequency details, yielding robust super-resolution performance in the compression scenario. Experimental results demonstrate that our solution produces visually pleasing enlargements for various web images/videos.
</div>


**Image Hallucination with Feature Enhancement** <br>
*Zhiwei Xiong, Xiaoyan Sun, Feng Wu* <br>
<span><pub>IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2009</pub></span> <br>
[PDF](https://ieeexplore.ieee.org/abstract/document/5206630/) |
<a onclick='expandABS("xiong09")'> Abstract </a>
<div style="display: none;" class=abs id="xiong09"><br>
Example-based super-resolution recovers missing high frequencies in a magnified image by learning the correspondence between co-occurrence examples at two different resolution levels. As high-resolution examples usually contain more details and are of higher dimensionality in comparison with low-resolution ones, the mapping from low-resolution to high-resolution is an ill-posed problem. Rather than imposing more complicated mapping constraints, we propose to improve the mapping accuracy by enhancing low-resolution examples in terms of mapped features, e.g., derivatives and primitives. A feature enhancement method is presented through a combination of interpolation with prefiltering and non-blind sparse prior deblurring. By enhancing low-resolution examples, unique feature information carried by high-resolution examples is decreased. This regularization reduces the intrinsic dimensionality disparity between two different resolution examples and thus improves the feature mapping accuracy. Experiments demonstrate our super-resolution scheme with feature enhancement produces high quality results both perceptually and quantitatively.

</div>
