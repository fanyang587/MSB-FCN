## Multi-Scale Bidirectional FCN for Object Skeleton Extraction

by Fan Yang, Xin Li, Hong Cheng, Yuxiao Guo, Leiting Chen and Jianping Li

### Introduction

This repository is for '[Multi-Scale Bidirectional FCN for Object Skeleton Extraction]'.
### Installation

For installation, please follow the instructions of [Caffe](https://github.com/BVLC/caffe).

The code has been tested successfully on Ubuntu 14.04 with CUDA 8.0.

### Usage

1. Clone the repository:

   ```shell
   git clone https://github.com/fanyang587/MSB-FCN.git
   ```

2. Build Caffe and pycaffe:

   ```shell
   cd caffe-master
   cp Makefile.config.example Makefile.config
   vim Makefile.config
   make -j8 && make pycaffe
   ```
ps: You should uncomment 'WITH_PYTHON_LAYER := 1' in Makefile.config before compiling.


3. Test:

   - Test code is in folder 'test'.
    - We provide two models trained with 10K and 30K training images. Download trained models and put them in folder 'code/models':
     - Sym-PASCAL dataset: [BaiduYun]() or [GoogleDrive](https://drive.google.com/open?id=17j6pw_ML1SUN52LA50lpzWifPjKAnidJ)
     - SK506 dataset: [BaiduYun]() or [GoogleDrive](https://drive.google.com/open?id=1zflZLDciS5_Ttljenia_nkkBOZBM7VBs)
     - SK1491 dataset: [BaiduYun]() or [GoogleDrive](https://drive.google.com/open?id=1zflZLDciS5_Ttljenia_nkkBOZBM7VBs)
     -  WH-SYMMAX: [BaiduYun]() or [GoogleDrive](https://drive.google.com/open?id=1zflZLDciS5_Ttljenia_nkkBOZBM7VBs)
   - Put the test images in folder 'images', and run
   
   ```shell
   python test.py
   ```
   -After that, the results will be genrated in folder 'result'.
### Citation
If C2SNet is useful for your research, please consider citing:

    @InProceedings{Yang_2018_AAAI,
	author = {Yang, Fan and Li, Xin and Cheng, Hong and Guo, Yuxiao and Chen, Leiting and Li, Jianping},
	title = {Multi-Scale Bidirectional FCN for Object Skeleton Extraction},
	booktitle = {AAAI},
	month = {February},
	year = {2018}
    }

### Question
Please contact 'fanyang_uestc@hotmail.com'
