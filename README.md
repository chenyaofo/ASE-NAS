# Automatic Subspace Evoking for Efficient Neural Architecture Search

![](https://img.shields.io/badge/-PyTorch%20Implementation-blue.svg?logo=pytorch)
![](https://img.shields.io/badge/license-MIT-blue.svg)

## Introduction

Neural Architecture Search (NAS) aims to automatically find effective architectures from a predefined search space. However, the search space is often extremely large. As a result, directly searching in such a large search space is non-trivial and also very time-consuming. To address above issues, we limit the search space to a small but effective subspace in each search step to boost both search performance and search efficiency. To this end, we propose a novel Neural Architecture Search method via Automatic Subspace Evoking (ASE-NAS) that finds promising architectures in automatically evoked subspaces. Specifically, in each search step, we first perform a global search, i.e., automatic subspace evoking, to find a good subspace from a set of candidate subspaces.  Then, we perform a local search within the searched subspace to obtain the resultant architecture. More critically, regarding the global search, we can further boost our ASE-NAS by taking well-designed/searched architectures as prior knowledge when constructing candidate subspaces. Extensive experiments show that our ASE-NAS not only greatly reduces the search cost but also finds better architectures than state-of-the-art methods in several benchmark search spaces (e.g., MobileNet-like space).

<p align="center">
<img src="assets/ase_nas_illustration.png" alt="ASE-NAS" width="95%" align=center />
</p>

## Requirements

Please install all the requirements in `requirements.txt`.

## Data preparation

Download and extract ImageNet train and val images from http://image-net.org/.
The directory structure is the standard layout for the torchvision [`datasets.ImageFolder`](https://pytorch.org/docs/stable/torchvision/datasets.html#imagefolder), and the training and validation data is expected to be in the `train` folder and `val` folder respectively:

```
/path/to/imagenet/
  train/
    class1/
      img1.jpeg
    class2/
      img2.jpeg
  val/
    class1/
      img3.jpeg
    class/2
      img4.jpeg
```

## Training Method

TODO
