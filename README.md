Depth-reconstruction from Light Field Data

# Application instruction of depth reconstruction algorithm v.2.0

# 基于优化建模的光场数据场景深度重建：项目简介：
三维重建是利用二维投影信息恢复三维场景的计算过程。其首要问题就是第三维信息，即物体深度信息的获取。深度是空间中的一点到相机所在平面的距离。光场数据记录了光线的空间位置和角度信息，可以实现高精度的物体三维表面重构。光场数据不同视点图像之间是通过视差来耦合的，该项目**利用四维光场的空-角关系重建场景的视差**。根据光场数据可视化的形式，可把场景深度重建算法划分三类：基于宏像素形式的光场数据场景深度重建（参见算法1-4）；基于Epi图像形式的光场数据场景深度重建（参见算法6-7）；基于子孔径图像形式的光场数据场景深度重建（参见算法8-12）。其中，本文独创算法是1、2、3、4、6、7、8、11、12；所有算法中1、8的效率和精度最高，8算法与立体视觉相比有跨越式的区别。

C++、python版本稍后奉上！

4D光场数据场景深度提取算法（自适应、C++版本）：
https://github.com/tzslg/Depth-Reconstruction-based-on-4D-light-field-data
# 深度重建的意义
1.传统计算机视觉相关算法，用二维特征解释三维信息，通常具有二义性。通常采用额外计算代价来优化所得的结果。高精度的深度信息的获取，可以为传统计算视觉相关的算法提供更精准高效的建模方式，进而提高计算视觉相关算法的性能。

2.利用深度信息可以重建出物体三维表面。
  三维表面重建和CT内部重建可以建立古代文物数据库，对文物的发掘和保护有很大帮助。
  AI是未来的发展趋势，AR、VR、虚拟试衣、人机交互、自动驾驶等领域都离不开三维重建技术的支持。
  此外，三维表面重建在电影、游戏、医疗、建筑行业等领域都有广阔的应用前景。


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
相似程度加权算法（自动去遮挡、噪声，效果最好）

### 2.Var
区域加权方差算法

### 3.Hist
灰度直方图峰值算法

### 4.NorF
频域归一化基频算法

### 5.CAE
角度熵
Williem, I. K. Park and K. M. Lee, "Robust Light Field Depth Estimation Using Occlusion-Noise Aware Data Costs," in IEEE Transactions on Pattern Analysis and Machine Intelligence, vol. 40, no. 10, pp. 2484-2497, 1 Oct. 2018, doi: 10.1109/TPAMI.2017.2746858.
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
