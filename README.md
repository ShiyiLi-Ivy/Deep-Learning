# Deep-Learning
使用 ResNet-18 作为 baseline 在CIFAR-100上训练并测试；对比cutmix，cutout，mixup 三种方法以及 baseline 方法在 CIFAR-100 图像分类任务中的性能表现；对三张训练样本分别经过 cutmix,  cutout, mixup 后进行可视化，一共show 9张图像。

## 训练步骤
运行 DataLoading，Data Augmentation，Model，Training 部分的代码，训练部分参考 Experiments。

## 数据增强
在实验中，使用了三种数据增强方法：CutMix、Cutout 和 Mixup。使用 cut 和 mix 两个布尔变量来控制是否进行 CutMix。如果 cut=True 且 mix=False，则进行 Cutout；如果 cut=False 且 mix=True，则进行 Mixup；如果 cut=True 且 mix=True，则进行 CutMix。
