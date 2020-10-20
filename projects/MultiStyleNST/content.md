---
layout: default
title: Multi-Style Sematic Style Transfer | 
---

# Multi-Style Sematic Style Transfer 
This project is aimed to transfer different semantic objects in one image into different styles. We use pretrained semantic segmentation model (DeepLab-V3) to get the foregound and backgound region, and apply style transfer on different style for each region. In addition to style loss and content loss in traditional neural style transfer, we futher add style-blending loss and total variance loss to make the result more harmony when blending very different style. Also, we provide custom control of blending effect. 

## Model Architecture

<img src = "./model_architecture.png" class="projectImg">