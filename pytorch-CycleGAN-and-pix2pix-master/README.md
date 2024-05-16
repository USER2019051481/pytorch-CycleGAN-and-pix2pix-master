
## 运行环境
- Windows
- Python 3.9
- Anaconda3 2024.02-1
- PyCharm Community Edition 2023.2.1
- CPU 

## 开始
### 安装

- 安装 [PyTorch](http://pytorch.org) 以及其他依赖项(e.g., torchvision, [visdom](https://github.com/facebookresearch/visdom) and [dominate](https://github.com/Knio/dominate)).
  - Conda用户，使用以下命令安装Conda环境 `conda env create -f environment.yml`.
  - 在pycharm中导入Anaconda3中配置好的环境
### 训练模型
- 下载数据集
- 数据集地址:https://efrosgans.eecs.berkeley.edu/pix2pix/datasets/
- 本项目采用了下载了其中的facades.tar.gz
- 查看训练结果和损失图，运行 `python -m visdom.server` 并单击 URL http://localhost:8097.

```bash
#!./scripts/train_pix2pix.sh
python train.py --dataroot ./datasets/facades --name facades_pix2pix --model pix2pix --direction BtoA
```
### 训练的结果
- 结果存放地址： checkpoints