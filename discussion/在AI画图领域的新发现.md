# 在AI画图领域的新发现 - Stable Diffusion（SD）

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [在AI画图领域的新发现 - Stable Diffusion（SD）](#在ai画图领域的新发现---stable-diffusionsd)
  - [SD的运行原理](#sd的运行原理)
  - [术语学习](#术语学习)
  - [采样器](#采样器)

<!-- /code_chunk_output -->

## SD的运行原理

Stable Diffusion（SD）是一个用于生成图像的深度学习模型。其运行原理如下：

1. **加噪声模糊处理**：首先，SD将一张图像进行加噪声模糊处理，这个过程使图像变得模糊且包含噪声。

2. **特征提取**：SD通过深度学习从原始图像中提取特征信息，这些特征包括图像的结构、纹理、颜色等。

3. **扩散过程**：SD通过对大量图像进行类似的操作逐渐开始理解这个扩散的过程。这意味着它学会了如何从噪声和模糊的图像中提取有用的信息。

4. **生成图像**：最后，SD执行模糊化的“逆过程”，从而生成具有特定内容的图像。这一步是将特征信息还原到图像中的过程，生成清晰的图像。

## 术语学习

在SD的真实绘制过程中，涉及到许多术语和概念。为了更好地理解和使用SD，建议查找相关文献进行学习和深入研究。

## 采样器

SD使用多种采样器来生成图像。以下是SD 1.6版本中的一些采样器：

- 老派采样器：
  - LMS
  - LMS Karras
  - Heun
  - Eular
  - Eular a
  - DDIM
  - PLMS

- DPM采样器：
  - DPM fast
  - DPM adaptive
  - DPM++SDE
  - DPM++SDE Karras
  - DPM++2S a
  - DPM++2S a Karras
  - DPM++2M
  - DPM++2M Karras
  - DPM++2M SDE
  - DPM++2M SDE Heun
  - DPM++2M SDE Heun Karras
  - DPM++2M SDE Heun Exponential
  - DPM++2M SDE Exponential
  - DPM++2M SDE Karras
  - DPM++3M SDE
  - DPM++3M SDE Karras
  - DPM++3M SDE Exponential
  - DPM2
  - DPM2a
  - DPM2 Karras
  - DPM2 a Karras

- 新派采样器：
  - UniPC
  - Restart

在以上30种采样器中，DPM系列最为复杂，有两个版本，以DPM、DPM++开头的都是改良版，DPM2开头的是第二代。SDE表示“随机微分方程”算法，这个算法效果更好，但计算时间较长。但是用时较长，其它采样器直接参考[视频](https://player.bilibili.com/player.html?bvid=BV1FN411i7sB&autoplay=false)

最终，根据速度和效果优先的原则，可以选择以下几个可用的采样器：

- 老派：Eular、Eular a
- DPM：++2M K、++SDE K、++2 SDE K、++2M SDE Ex、++3M SDE K、++3M SDE Ex
- 新派：UniPC、Restart
