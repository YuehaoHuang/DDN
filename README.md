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
pip install torch==1.10.1+cu111 torchvision==0.11.2+cu111 torchaudio==0.10.1 -f https://download.pytorch.org/whl/cu111/torch_stable.html
pip install -r requirements.txt
```

## 数据集

### 指令数据集

从[指令数据集](https://pan.baidu.com/s/1ocg2nHophmIKLTC_oMi8dQ?pwd=m6v2)下载

### 预训练数据集

从[预训练数据集](https://pan.baidu.com/s/1_1Eu6ejnCnsgEUiYFZUmjw?pwd=nr8h)下载

## 测试

### 导航策略测试

```
python test.py --mode=test_DDN --dataset_mode=test --seen_instruction=1 --device=cuda:0 --epoch=50
```
