## Multi-Scale Bidirectional FCN for Object Skeleton Extraction

by Fan Yang, Xin Li, Hong Cheng, Yuxiao Guo, Leiting Chen and Jianping Li

### Introduction

This repository is for '[Multi-Scale Bidirectional FCN for Object Skeleton Extraction](https://www.aaai.org/ocs/index.php/AAAI/AAAI18/paper/view/16722/16345)'.
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
    - Download the following pre-trained models and put them in folder 'test/models':
     - Sym-PASCAL dataset: [BaiduYun](https://pan.baidu.com/s/1qY0lUnJAYqyyr0HfF9-baA) or [GoogleDrive](https://drive.google.com/open?id=1aoehs3ywQ589yWJUrJMnsfRV4uxamJKb)
     - SK506 dataset: [BaiduYun](https://pan.baidu.com/s/1cRjFhrT2UPLwXSg_5ZEefg) or [GoogleDrive](https://drive.google.com/open?id=1spe2oI5feLWvDuiCnf_4mMkw1ibGcEhk)
     - SK1491 dataset: [BaiduYun](https://pan.baidu.com/s/1LANVVgiSFhYzjaL7LtEy3g) or [GoogleDrive](https://drive.google.com/open?id=1dfrju90JAAcMAq8KJBLD5OwPBjDWOZ_p)
     - WH-SYMMAX dataset: [BaiduYun](https://pan.baidu.com/s/1zWjPNf_0Fl-J2HNK_FShKw) or [GoogleDrive](https://drive.google.com/open?id=13WbB5oMoYqJe4oHQmVEUz2bzitp0ZGuw)
   - Put the test images in folder 'images', and run
   
   ```shell
   python test.py
   ```
   -After that, the results will be genrated in folder 'result'.
### Citation
If MSB-FCN is useful for your research, please consider citing:

     @inproceedings{Yang_2018_AAAI,
        author = {Yang, Fan and Li, Xin and Cheng, Hong and Guo, Yuxiao and Chen, Leiting and Li, Jianping},
        title = {Multi-Scale Bidirectional FCN for Object Skeleton Extraction},
        booktitle = {AAAI},
        month = {February}
        year = {2018}
      }

### Question
Please contact 'fanyang_uestc@hotmail.com'
