---
layout: default
title: Multi-Style Sematic Style Transfer | 
---
<div>
	<h1 style="display:inline;"> Multi-Style Sematic Style Transfer </h1> 
	<a href="https://github.com/aa10402tw/MultiStyle-Semantic-Style-Transfer"> [Code] </a> 
</div>
This project is aimed to transfer different semantic objects in one image into different styles. We use pretrained semantic segmentation model (DeepLab-V3) to get the foregound and backgound region, and apply style transfer on different style for each region. In addition to style loss and content loss in traditional neural style transfer, we futher add style-blending loss and total variance loss to make the result more harmony when blending very different style. Also, we provide custom control of blending effect. 

## Model Architecture
<img src = "./model_architecture.png" class="projectDetailImg">
Given one image I<sub>src</sub> and two target style images I<sub>s1</sub> and I<sub>s2</sub>, we want to transfer different semantic objects into different style accrodingly. We first produced two intermediated result image I<sub>i1</sub> and I<sub>i2</sub>, and compute the style loss between (I<sub>s1</sub>, I<sub>i1</sub>) and (I<sub>s2</sub>, I<sub>i2</sub>). The we merge these two intermediated images into final result image I<sub>result</sub> by semantic map predicted by DeepLab-V3 image. Finally compute the content loss between (I<sub>src</sub>, I<sub>result</sub>). Further more, to make the resulting image more harmony while blending different styles and prevent weird boundary after merging two intermediated images, we also compute the style-blending loss which is weighted style loss between (I<sub>s1</sub>, I<sub>i2</sub>) and (I<sub>s2</sub>, I<sub>ii</sub>), and smooth loss which is total variance of I<sub>result</sub>. The entire loss function can be written as follow:<br/>
L = &lambda;<sub>1</sub>L<sub>style</sub> + &lambda;<sub>2</sub>L<sub>blend</sub> + &lambda;<sub>3</sub>L<sub>content</sub> + &lambda;<sub>4</sub>L<sub>Smooth</sub>
&nbsp;

## Result 
### Compare with naive approach
<img src = "./compare.png" class="projectDetailImg">

### Style Blending Ratio
<img src = "./blending.png" class="projectDetailImg">

### Sample Result
<img src="./result_1.png" width="40%"> <img src="./result_2.png" width="40%">

### Video Style Transfer
<img src="./video_1.gif" width="40%"> <img src="./video_2.gif" width="40%">

