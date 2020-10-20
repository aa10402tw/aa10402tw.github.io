---
layout: default
title: Multi-Style Sematic Style Transfer | 
---

# Multi-Style Sematic Style Transfer 
This project is aimed to transfer different semantic objects in one image into different styles. We use pretrained semantic segmentation model (DeepLab-V3) to get the foregound and backgound region, and apply style transfer on different style for each region. In addition to style loss and content loss in traditional neural style transfer, we futher add style-blending loss and total variance loss to make the result more harmony when blending very different style. Also, we provide custom control of blending effect. 

## Model Architecture
<img src = "./model_architecture.png" class="projectDetailImg">
Given one image I<sub>src</sub> and two target style images I<sub>s1</sub> and I<sub>s2</sub>, we transfer the different semantic objects into different style accrodingly. We first produced two intermediated result image I<sub>i1</sub> and I<sub>i2</sub>, and compute the style loss between (I<sub>s1</sub>, I<sub>i1</sub>) and (I<sub>s2</sub>, I<sub>i2</sub>).
