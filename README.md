# Find What You Want: Learning Demand-conditioned Object Attribute Space for Demand-driven Navigation

## 概述
<img src="demo/NIPS-2023-DDN.gif" align="middle" width="700"/> 

提出了一种需求驱动的导航任务，它需要一个代理来找到满足人类需求的对象，并提出了一个新的方法来解决这个任务

## 环境配置

```bash
git clone https://github.com/YuehaoHuang/DDN.git
cd DDN
conda create -n ddn python=3.9 -y
source activate ddn
pip install torch==1.10.1+cu111 torchvision==0.11.2+cu111 torchaudio==0.10.1 -f 
pip install -r requirements.txt
```

## 数据集

### 指令数据集

从[指令数据集](http://ceres-solver.org/ceres-solver-2.0.0.tar.gz)下载

### 预生成数据集

从[预生成数据集](http://ceres-solver.org/ceres-solver-2.0.0.tar.gz)下载

### 预训练数据集

从[预训练数据集](http://ceres-solver.org/ceres-solver-2.0.0.tar.gz)下载

## 测试

### 导航策略测试

```
python eval.py --mode=test_DDN --eval_path=$path_to_saved_model$ --dataset_mode=$train,test$ --seen_instruction=$0,1$  --device=cuda:0 --epoch=500 --eval_ckpt=$idx$
```

对于参数“dataset_mode”，“train”表示“seen_scene”，而“test”表示“unseen scene”。在测试过程中选择其中一个。
对于参数“seen_instruction”，“1”表示“seen_direction”，而“0”表示“unseen_scene”。在测试过程中选择其中一个。