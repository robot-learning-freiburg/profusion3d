# Progressive Multi-Modal Fusion for Robust 3D Object Detection

ProFusion3D is a progressive fusion framework that combines features in both Bird's Eye View (BEV) and Perspective View (PV) at both intermediate and object query levels. Our architecture hierarchically fuses local and global features, enhancing the robustness of 3D object detection.

![Overview of Profusion3D Architecture](http://profusion3d.cs.uni-freiburg.de/static/images/figures/main_arch_web3.png)

This repository contains the **PyTorch implementation** of our CoRL'2024 paper [Progressive Multi-Modal Fusion for Robust 3D Object Detection](https://arxiv.org/pdf/2410.07475.pdf). The repository builds on [MMDetection3D](https://github.com/open-mmlab/mmdetection3d).

If you find this code useful for your research, we kindly ask you to consider citing our papers:

```
@article{mohan2024progressive,
  title={Progressive Multi-Modal Fusion for Robust
	3D Object Detection},
  shorttile={ProFusion3D},
  author={Mohan, Rohit and Cattaneo, Daniele and Drews, Florian and Valada, Abhinav},
  journal={Conference on Robot Learning (CoRL)},
  year={2024}
}
```

##  Installation
Please refer to the [MMDetection3D documentation](https://mmdetection3d.readthedocs.io/en/latest/get_started.html) for detailed instructions.

## Dataset Preparation
Please refer to the official MMDetection3D documentation for instructions on processing the nuScenes dataset: MMDetection3D - nuScenes Dataset Preparation(https://mmdetection3d.readthedocs.io/en/latest/datasets/nuscenes_det.html).

## Usage
```bash
# Training
bash tools/dist_train.sh /path/to/your/config 8

# Inference
bash tools/dist_test.sh /path/to/your/config /path/to/your/checkpoint.pth 8 --eval bbox
```

## Pre-Trained Models
Pre-trained models can be found in the [model zoo](./MODEL_ZOO.md).

## Acknowledgements
We have used utility functions from other open-source projects. We espeicially thank the authors of:
- [MMDetection3D](https://github.com/open-mmlab/mmdetection3d)

## Contacts
* [Rohit Mohan](https://github.com/mohan1914)