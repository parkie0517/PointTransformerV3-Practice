# PointTransformerV3-Practice
PointTransformerv3 practice using PyTorch

## 1. What is this for?
Q. Yeah, what's this repo for?
A. 
Q. What's the purpose of writing a README file?
A. I'm keeping track of the steps I take for future reference.

## 2. GPU Specification
I am using 4 A6000 GPUs.

## 3. Installation
Follow the steps below
- conda update -n base -c anaconda conda ✅
- conda create -n pointcept python=3.8 -y ✅
- conda activate pointcept ✅
- conda install -y ninja ✅

The authors of PointTransformerV3 used CUDA==11.8 and PyTorch==2.1.0 (this job might take long)
- conda install pytorch==2.1.0 torchvision==0.16.0 torchaudio==2.1.0 pytorch-cuda=11.8 -c pytorch -c nvidia ✅
- conda install -y nvidia/label/cuda-11.8.0::cuda-toolkit ✅

Check if CUDA is available ✅
- pytorch
- import torch
- torch.cuda.is_available()

Continue on with the installation process
- conda install h5py pyyaml -c anaconda -y ✅
- conda install sharedarray tensorboard tensorboardx yapf addict einops scipy plyfile termcolor timm -c conda-forge -y ✅
- conda install pytorch-cluster pytorch-scatter pytorch-sparse -c pyg -y ✅
- pip install torch-geometric ✅


- git clone https://github.com/Pointcept/PointTransformerV3.git ✅
- cd ./Pointcept/libs/pointops
- python setup.py install

Make sure you are downloading the version that matches your CUDA version
- pip install spconv-cu118 ✅

This is optional
- pip install open3d ✅

Okay continue on! Let's install FlashAttention
- pip install flash-attn --no-build-isolation ✅

## Dataset Preparation
I will use S3DIS.
