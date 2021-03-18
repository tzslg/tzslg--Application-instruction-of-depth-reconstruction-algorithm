Depth-reconstruction from Light Field Data

# Application instruction of depth reconstruction algorithm v.2.0

# 基于优化建模的光场数据场景深度重建：项目简介：
三维重建是利用二维投影信息恢复三维场景的计算过程。其首要问题就是第三维信息，即物体深度信息的获取。深度是空间中的一点到相机所在平面的距离。光场数据记录了光线的空间位置和角度信息，可以实现高精度的物体三维表面重构。光场数据不同视点图像之间是通过视差来耦合的，该项目**利用四维光场的空-角关系重建场景的视差**。根据光场数据可视化的形式，可把场景深度重建算法划分三类：基于宏像素形式的光场数据场景深度重建（参见算法1-5）；基于Epi图像形式的光场数据场景深度重建（参见算法6-7）；基于子孔径图像形式的光场数据场景深度重建（参见算法8-12）。其中项目独创算法是1、2、4、5、6、7、8、11、12。

C++、python版本稍后奉上！

4D光场数据场景深度提取算法（自适应、C++版本）：
https://github.com/tzslg/Depth-Reconstruction-based-on-4D-light-field-data

## How to use：
(This software is tested using Matlab 2019b with Windows10 64bit environment)

Step 1: initialization/初始化

Step 2: related parameter setting/相关参数设置

Step 3: load data/加载光场数据
光场数据的形式可以是子孔径图像或全光图像。

Step 4: select reconstruction algorithm and optimization algorithm/选择重建的算法

Step 5: select optimization algorithm/选择优化的算法

Step 6: save the results/保存视差重建的结果

## Reconstruction algorithm part

相关算法描述，待补充（毕业后补充）。

### 1.Nor
角度域相似程度加权（自动去遮挡、噪声，效果最好）

### 2.Var
角度域区域加权方差

### 3.CAE
角度域角度熵，参考文献[3]

### 4.NorF
角度域傅里叶变化归一化基频

### 5.Hist
角度域灰度直方图峰值

### 6.EPI-SP
搜索点二分算法

### 7.EPI-Kalm
kalman修正搜索点算法

### 8.Cor
空间域匹配窗口一致性

### 9.MWTA
空间域多窗口

### 10.wM
空间域常系数

### 11.Adaptive region matching for scene depth reconstruction from light field data
基于匹配熵正则化场景深度重建

### 12.Depth reconstruction from light field based on monomer subset data
单体化场景深度重建


### CONTACT:

Ligen(ligenshi@88.com)

未完待续
