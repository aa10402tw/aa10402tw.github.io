---
layout: default
title: Distributed Hyper-Parameters Optimization | 
---
<div>
	<h1 style="display:inline;"> Distributed Hyper-Parameters Optimization </h1> 
	<a href="https://github.com/aa10402tw/Distributed-Hyper-Parameters-Optimization"> [Code] </a> 
</div>
Hyper-parameters optimization problem is aimed to find the most suitable hyper-parameters for training neural network. This project use Grid Search, Random Search and Evoluationary Search to tackle hyper-parameters optimization problem, and use CUDA-Awared MPI (Distributed Computing) to accerlate the process. We achieve 3.65 to 3.8 speedup under 4 nodes.

## Hyper-parameters optimization 
<img src = "./images/DHPO/HBO.png" class="projectDetailImg">

## Result 
### Accuracy Comparison
<img src="./images/DHPO/mnist_acc.png" width="40%"> <img src="./images/DHPO/cifar10_acc.png" width="40%">

### Speedup
<img src="./images/DHPO/mnist_speedup.png" width="40%"> <img src="./images/DHPO/cifar10_speedup.png" width="40%">