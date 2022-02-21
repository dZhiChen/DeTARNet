
# DetarNet: Decoupling Translation and Rotation by Siamese Network for Point Cloud Registration

<!-- [[arXiv]](https://arxiv.org) -->

## Introduction
Point cloud registration is a fundamental step for many tasks. In this paper, we propose a neural network named DetarNet to decouple the translation $t$ and rotation $R$, so as to overcome the performance degradation due to their mutual interference in point cloud registration.
First, a Siamese Network based Progressive and Coherent Feature Drift (PCFD) module is proposed to align the source and target points in high-dimensional feature space, and accurately recover translation from the alignment process. Then we propose a Consensus Encoding Unit (CEU) to construct more distinguishable features for a set of putative correspondences. After that, a Spatial and Channel Attention (SCA) block is adopted to build a classification network for finding good correspondences. Finally, the rotation is obtained by Singular Value Decomposition (SVD). In this way, the proposed network decouples the estimation of translation and rotation, resulting in better performance for both of them. 
Experimental results demonstrate that the proposed DetarNet improves registration performance on both indoor and outdoor scenes.
![](misc/pipeline.png)

## Configuration
The code has been tested with Python 3.6 on Ubuntu 16.04. The cuda version we use is CUDA10.2.
If you are using conda, you may configure DetarNet as:
``` bash
conda create -n DetarNet python=3.6
pip install -r requirements.txt
source activate DetarNet
