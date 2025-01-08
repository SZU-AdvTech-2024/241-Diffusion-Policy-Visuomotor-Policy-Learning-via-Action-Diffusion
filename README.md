# Diffusion Policy 实验

## 项目简介

本项目实现了基于扩散模型的策略学习，用于解决机器人操控任务。扩散模型通过逐步去噪的方式生成动作序列，从而实现对复杂任务的有效控制。本项目使用了 Metaworld 环境中的 `shelf-place-v2` 任务进行实验验证。

## 环境依赖

- Python 3.10
- PyTorch 1.13.1
- torchvision 0.14.1
- diffusers
- huggingface_hub
- scikit-image 0.19.3
- scikit-video 1.1.11
- zarr
- numcodecs
- gym 0.26.2
- pygame 2.1.2
- pymunk 6.2.1
- shapely 1.8.4

## 文件说明

metaworld_expert.ipynb 收集metaworld中专家策略生成的成功轨迹，保存为zarr文件

diffusion_policy_vision_resnet+tf_shelf_place.ipynb 训练resnet+transformer的策略网络，并在metaworld环境推理

diffusion_policy_vision_resnet+unet_shelf_place.ipynb 训练resnet+Unet的策略网络，并在metaworld环境推理