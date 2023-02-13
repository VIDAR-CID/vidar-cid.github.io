---
title: 'Anchor-Free Object Detection'
date: 2020-04-12
permalink: /posts/2020/04/anchor-free/
tags:
  - Object Detection
---

Summarizing recent anchor-free object detectors.

## CornerNet: Detecting Objects as Paired Keypoints - ECCV 2018

![CornerNet: Detecting Objects as Paired Keypoints - ECCV 2018](https://i.imgur.com/npESC4v.jpg)

The model detect an object as a pair of bounding box corners grouped together. A convolutional network outputs a heatmap for all top-left corners, a heatmap for all bottom-right corners, and an embedding vector for each detected corner. The network is trained to predict similar embeddings for corners that belong to the same object.

![CornerNet: Detecting Objects as Paired Keypoints - ECCV 2018](https://i.imgur.com/wHrOzEW.jpg)

The backbone network is followed by two prediction modules, one for the top-left corners and the other for the bottom-right corners. Using the predictions from both modules, we locate and group the corners.

![CornerNet: Detecting Objects as Paired Keypoints - ECCV 2018](https://i.imgur.com/YyHEujb.jpg)


### Code

[PyTorch](https://github.com/princeton-vl/CornerNet)






## CornerNet-Lite: Efficient Keypoint Based Object Detection


CornerNet-Saccade speeds up inference by reducing the number of pixels to process. It uses an attention mechanism similar to saccades in human vision. It starts with a downsized full image and generates an attention map, which is then zoomed in on and processed further by the model. This differs from the original CornerNet in that it is applied fully convolutionally across multiple scales.

![CornerNet-Lite: Efficient Keypoint Based Object Detection](https://i.imgur.com/Zzu1wRl.jpg)

We predict a set of possible object locations from the attention maps and bounding boxes generated on a downsized full image. We zoom into each location and crop a small region around that location. Then we detect objects in each region. We control the efficiency by ranking the object locations and choosing top k locations to process. Finally, we merge the detections by NMS.

![CornerNet-Lite: Efficient Keypoint Based Object Detection](https://i.imgur.com/DTkcDKz.png)

CornerNet-Squeeze speeds up inference by reducing the amount of processing per pixel. It incorporates ideas from SqueezeNet and MobileNets, and introduces a new, compact hourglass backbone that makes extensive use of 1×1 convolution, bottleneck layer, and depth-wise separable convolution.

![CornerNet-Lite: Efficient Keypoint Based Object Detection](https://i.imgur.com/iXqDI10.png)

### Code




## (ExtremeNet)Bottom-up Object Detection by Grouping Extreme and Center Points - CVPR 2019

![(ExtremeNet)Bottom-up Object Detection by Grouping Extreme and Center Points - CVPR 2019](https://i.imgur.com/AsbOUJw.png)

In this paper, we propose ExtremeNet, a bottom-up object detection framework that detects four extreme points (top-most, left-most, bottom-most, right-most) of an object. We use a state-of-the-art keypoint estimation framework to find extreme points, by predicting four multi-peak heatmaps for each object category. In addition, we use one heatmap per category predicting the object center, as the average of two bounding box edges in both the x and y dimension. We group extreme points into objects with a purely geometry-based approach. We group four extreme points, one from each map, if and only if their geometric center is predicted in the center heatmap with a score higher than a pre-defined threshold. We enumerate all $O(n^4)$combinations of extreme point prediction, and select the valid ones.

![(ExtremeNet)Bottom-up Object Detection by Grouping Extreme and Center Points - CVPR 2019](https://i.imgur.com/Ek7WhEw.png)

Given four extreme points t, b, r, l extracted from heatmaps Ŷ (t) , Ŷ (l) , Ŷ (b) , Ŷ (r), we compute their geometric center $c=\left(\frac{l_{x}+t_{x}}{2}, \frac{t_{y}+b_{y}}{2}\right)$. If this center is predicted2 2with a high response in the center map Ŷ (c), we commit the extreme points as a valid detection: Ŷcx ,cy ≥ τc for a threshold τc. We then enumerate over all quadruples of keypoints t, b, r, l in a brute force manner. We extract detections foreach class independently. 


![(ExtremeNet)Bottom-up Object Detection by Grouping Extreme and Center Points - CVPR 2019](https://i.imgur.com/TYhe4Al.png)



### Code

[PyTorch](https://github.com/xingyizhou/ExtremeNet)



## (CenterNet-D)CenterNet: Keypoint Triplets for Object Detection - ICCV 2019

![(CenterNet-D)CenterNet: Keypoint Triplets for Object Detection - ICCV 2019](https://i.imgur.com/6pFsCoQ.png)

In this paper, we present a low-cost yet effective solution named CenterNet, which explores the central part of a proposal, i.e., the region that is close to the geometric center of a box, with one extra keypoint. We intuit that if a predicted bounding box has a high IoU with the ground-truth box, then the probability that the center keypoint in the central region of the bounding box will be predicted as the same class is high, and vice versa. Thus, during inference, after a proposal is generated as a pair of corner keypoints, we determine if the proposal is indeed an object by checking if there is a center keypoint of the same class falling within its central region.

![(CenterNet-D)CenterNet: Keypoint Triplets for Object Detection - ICCV 2019](https://i.imgur.com/MFkqXVY.jpg)

A convolutional backboneoutput two corner heatmaps and a center keypoint heatmap, respectively.the similar embeddings are used to detect a potential boundingthe final bounding boxes. network applies cascade corner pooling and center pooling to Similar to CornerNet, a pair of detected corners and box. Then the detected center keypoints are used to determine the final bounding boxes.

![(CenterNet-D)CenterNet: Keypoint Triplets for Object Detection - ICCV 2019](https://i.imgur.com/ozuZHNW.jpg)



### Code

[PyTorch](https://github.com/Duankaiwen/CenterNet)



## (CenterNet-Z)Objects as Points

![(CenterNet-Z)Objects as Points](https://i.imgur.com/OCXfp70.png)

We represent objects by a single point at their bounding box center. Other properties, such as object size, dimension, 3D extent, orientation, and pose are then regressed directly from image features at the center location. Object detection is then a standard keypoint estimation problem. We simply feed the input image to a fully convolutional network that generates a heatmap. Peaks in this heatmap correspond to object centers. Image features at each peak predict the objects bounding box height and weight. The model trains using standard dense supervised learning. Inference is a single network forward-pass, without non-maximal suppression for post-processing.

![(CenterNet-Z)Objects as Points](https://i.imgur.com/qwbBPGi.png)

The numbers in the boxes represent the stride to the image. (a): Hourglass Network, We
use it as is in CornerNet.. (b): ResNet with transpose convolutions. We add one 3 × 3 deformable convolutional layer before each up-sampling layer. Specifically, we first use deformable convolution to change the channels and then use transposed convolution to upsample the feature map (such two steps are shown separately in 32 → 16. We show these two steps together as a dashed arrow for 16 → 8 and 8 → 4). (c): The original DLA-34 for semantic segmentation. (d): Our modified DLA-34. We add more skip connections from the bottom layers and upgrade every convolutional layer in upsampling stages to deformable convolutional layer.

!(CenterNet-Z)Objects as Points[](https://i.imgur.com/GA6wNG7.png)


### Code

[PyTorch](https://github.com/xingyizhou/CenterNet)



## (FSAF)Feature Selective Anchor-Free Module for Single-Shot Object Detection - CVPR 2019



![(FSAF)Feature Selective Anchor-Free Module for Single-Shot Object Detection - CVPR 2019](https://i.imgur.com/ObEG4iU.png)



Our motivation is to let each instance select the best level of feature freely to optimize the network, so there should be no anchor boxes to constrain the feature selection in our module. Instead, we encode the instances in an anchor-free manner to learn the parameters for classification and regression. An anchor-free branch is built per level of feature pyramid, independent to the anchor-based branch. Similar to the anchor-based branch, it consists of a classification subnet and a regression subnet. An instance can be assigned to arbitrary level of the anchor-free branch. During training, we dynamically select the most suitable level of feature for each instance based on the instance content instead of just the size of instance box. The selected level of feature then learns to detect the assigned instances. At inference, the FSAF module can run independently or jointly with anchor-based branches. 



![(FSAF)Feature Selective Anchor-Free Module for Single-Shot Object Detection - CVPR 2019](https://i.imgur.com/rspa42e.png)



The FSAF module only introduces two additional conv layers (dashed feature maps) per pyramid level, keeping the architecture fully convolutional.



![(FSAF)Feature Selective Anchor-Free Module for Single-Shot Object Detection - CVPR 2019](https://i.imgur.com/3tsiCZG.png)



Online feature selection mechanism. Each instance is passing through all levels of anchor-free branches to compute the averaged classification (focal) loss and regression (IoU) loss over effective regions. Then the level with minimal summation of two losses is selected to set up the supervision signals for that instance.



![](https://i.imgur.com/GmH06Q0.png)





## FoveaBox: Beyond Anchor-based Object Detector



![FoveaBox: Beyond Anchor-based Object Detector](https://i.imgur.com/Y5K4Uan.png)



FoveaBox is motivated from the fovea of human eyes: the center of the vision field (object) is with the highest visual acuity. FoveaBox jointly predicts the locations where the object’s center area is likely
to exist as well as the bounding box at each valid location. Thanks to the feature pyramidal representations, different scales of objects are naturally detected from multiple levels of features.



![FoveaBox: Beyond Anchor-based Object Detector](https://i.imgur.com/nTougKV.png)



The design of the architecture follows RetinaNet to make a fair comparison. FoveaBox uses a Feature Pyramid Network backbone on top of a feedforward ResNet architecture. To this backbone, FoveaBox attaches two subnetworks, one for classifying the corresponding cells and one for predict the (x1 , y1 , x2 , y2 ) of ground-truth object boxes. For each spatial output location, the FoveaBox predicts one score output for each class and the corresponding 4-dimensional box, which is different from previous works attaching A anchors in each position (usually A = 9).



![FoveaBox: Beyond Anchor-based Object Detector](https://i.imgur.com/ea6VsgH.png)





### Code

[PyTorch](https://github.com/taokong/FoveaBox)







## FCOS: Fully Convolutional One-Stage Object Detection - ICCV 2019

In order to suppress these low-quality detections, we introduce a novel “center-ness” branch (only one layer) to predict the deviation of a pixel to the center of its corresponding bounding box. This score is then used to down-weight low-quality detected bounding boxes and merge the detection results in NMS. The simple yet effective center-ness branch allows the FCN-based detector to outperform anchor-based counterparts under exactly the same training and testing settings.



![FCOS: Fully Convolutional One-Stage Object Detection - ICCV 2019](https://i.imgur.com/aKH5xYC.png)


The network architecture of FCOS, where C3, C4, and C5 denote the feature maps of the backbone network and P3 to P7 are the feature levels used for the final prediction. H × W is the height and width of feature maps. ‘/s’ (s = 8, 16, ..., 128) is the downsampling ratio of the feature maps at the level to the input image. As an example, all the numbers are computed with an 800 × 1024 input.



![FCOS: Fully Convolutional One-Stage Object Detection - ICCV 2019](https://i.imgur.com/JqIcW0A.png)


### Code

[PyTorch](https://github.com/tianzhi0549/FCOS)




## RepPoints: Point Set Representation for Object Detection - ICCV 2019

RepPoints is a set of points that learns to adaptively position themselves over an object in a manner that circumscribes the object’s spatial extent and indicates semantically significant local areas. The training of RepPoints is driven jointly by object localization and recognition targets, such that the RepPoints are tightly bound by the ground-truth bounding box and guide the detector toward correct object classification. This adaptive and differentiable representation can be coherently used across the different stages of a modern object detector, and does not require the use of anchors to sample over a space of bounding boxes.

![RepPoints: Point Set Representation for Object Detection - ICCV 2019](https://i.imgur.com/5fhfyee.jpg)


Overview of the proposed RPDet (RepPoints detector). Whilebone, we only draw the afterwards pipeline of one scale of FPN featureshare the same afterwards network architecture and the same model weights. feature pyramidal networks (FPN) are adopted as the backmaps for clear illustration. Note all scales of FPN feature maps share the same afterwards network architecture and the same model weights.

![RepPoints: Point Set Representation for Object Detection - ICCV 2019](https://i.imgur.com/UCX7qCq.png)



### Code

[PyTorch](https://github.com/microsoft/RepPoints)

  