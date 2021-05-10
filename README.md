# 飞桨常规赛∶遥感影像地块分割 -4月第三名方案


## 项目描述
### 训练数据集文件名称：train_and_label.zip

## 包含2个子文件，分别为：训练数据集（原始图片）文件、训练数据集（标注图片）文件，详细介绍如下：

* **训练数据集**（原始图片）文件名称：img_train

包含66,653张分辨率为2m/pixel，尺寸为256 * 256的JPG图片，每张图片的名称形如T000123.jpg。

* **训练数据集**（标注图片）文件名称：lab_train

包含66,653张分辨率为2m/pixel，尺寸为256 * 256的PNG图片，每张图片的名称形如T000123.png。

备注： 全部PNG图片共包括4种分类，像素值分别为0、1、2、3。此外，像素值255为未标注区域，表示对应区域的所属类别并不确定，在评测中也不会考虑这部分区域。

* **测试数据集**
测试数据集文件名称：img_test.zip，详细介绍如下：

包含4,609张分辨率为2m/pixel，尺寸为256 * 256的JPG图片，文件名称形如123.jpg。、

## 数据增强工具
**PaTTA:** 由第三方开发者组织AgentMaker维护的Test-Time Augmentation库，可在测试时通过数据增强方式产生额外的推理结果，在此基础上进行投票即可获得更稳定的成绩表现。 https://github.com/AgentMaker/PaTTA

**RIFLE:** 由第三方开发者对ICML 2020中的《RIFLE: Backpropagation in Depth for Deep Transfer Learning through Re-Initializing the Fully-connected LayEr》论文所提供的封装版本，其通过对输出层多次重新初始化来使得深层backbone得到更充分的更新。 https://github.com/GT-ZhangAcer/RIFLE_Module

## 1、解压数据集
## 2、图像预处理和增强
## 3、图像标签赋予含义，划分好训练集，测试集验证集
## 4、高层AIP定义模型，DeepLabv3p网络选择'Xception65'为骨干网络调好参数
## 5、model.train()调参训练
## 6、模型推理



## 项目结构
```
-|data
-|work
-README.MD
-Remote sensing of the game.ipynb
```
## 使用方式
A：在AI Studio上[运行本项目](https://aistudio.baidu.com/aistudio/projectdetail/1803811)
B：单步运行，全流程可以直接跑通。
