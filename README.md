# FASDD: An Open-access 100,000-level Flame And Smoke Detection Dataset for Deep Learning in Fire Detection

[Ming Wang](https://github.com/OyamingO), [Peng Yue](https://geos.whu.edu.cn/peng.html)*, Liangcun Jiang*, Dayu Yu, Tianyu Tuo, Jian Li

[[`Paper`](https://doi.org/10.57760/sciencedb.j00104.00103)] [[`Project`](https://github.com/OyamingO/Fire-And-Smoke-Detection-Dataset)] [[`Dataset`](https://doi.org/10.57760/sciencedb.j00104.00103)] [[`BibTeX`](#Citing-FASDD)]

> FASDD was developed by the research group led by [Prof. Peng Yue](https://geos.whu.edu.cn/peng.html) at Wuhan University.

### 🚀: FASDD source
<img src="assets/source.png?raw=true" width="88%" />

### 🚀: FASDD workflow
<img src="assets/workflow.png?raw=true" width="88%" />

## Installation
No custom code was developed for this work. However, to replicate the technical validation results, the Swin Transformer source code is available at: https://github.com/SwinTransformer/Swin-Transformer-Object-Detection. The following steps can be referred to for configuring the operating environment of the Swin Transformer model.

Step 1. Create a conda environment and activate it.
conda create --name openmmlab python=3.8 -y
conda activate openmmlab

Step 2. Install PyTorch following official instructions, e.g.
The code requires `python>=3.7`, as well as `pytorch>=1.7` and `torchvision>=0.8`. Please follow the instructions [here](https://pytorch.org/get-started/locally/) to install both PyTorch and TorchVision dependencies. Installing both PyTorch and TorchVision with CUDA support is strongly recommended.

Step 3. Install MMEngine and MMCV using MIM.
pip install -U openmim
mim install mmengine
mim install "mmcv>=2.0.0"
Note: In MMCV-v2.x, mmcv-full is rename to mmcv, if you want to install mmcv without CUDA ops, you can use mim install "mmcv-lite>=2.0.0rc1" to install the lite version.

Step 4. Install MMDetection.
Case a: If you develop and run mmdet directly, install it from source:
git clone https://github.com/open-mmlab/mmdetection.git
cd mmdetection
pip install -v -e .

The following optional dependencies are necessary for mask post-processing, saving masks in COCO format, the example notebooks, and exporting the model in ONNX format. `jupyter` is also required to run the example notebooks.
```
pip install opencv-python pycocotools matplotlib
```

## Citing FASDD

If you use FASDD in your research, please cite the following article:

```bibtex
@article{wang2025open,
  title={An open flame and smoke detection dataset for deep learning in remote sensing based fire detection},
  author={Wang, Ming and Yue, Peng and Jiang, Liangcun and Yu, Dayu and Tuo, Tianyu and Li, Jian},
  journal={Geo-spatial Information Science},
  volume={28},
  number={2},
  pages={511--526},
  year={2025},
  publisher={Taylor \& Francis},
  doi={10.1080/10095020.2024.2347922},
  url={https://doi.org/10.1080/10095020.2024.2347922}
}

```
