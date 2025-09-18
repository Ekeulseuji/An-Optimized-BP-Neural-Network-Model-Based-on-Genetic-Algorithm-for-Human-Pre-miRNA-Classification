### 经遗传算法优化的反向传播神经网络（用于分类任务）
#### An Optimized Genetic Algorithm-based BP Neural Network Model for the Classification of Human Pre-miRNA Subclasses

---

是我23年做的一个小项目 有发论文哦可以参考！

[论文链接 - 2024 IEEE 3rd International Conference on Electrical Engineering, Big Data and Algorithms (EEBDA)](https://ieeexplore.ieee.org/document/10485935 "2024 IEEE 3rd International Conference on Electrical Engineering, Big Data and Algorithms (EEBDA)")

有数模需求的同学可以直接用我传的代码实现GA-BPNN（从`GA-BPNN_Codes_and_Plots.ipynb`的第19格开始）

[![Open In Google Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Ekeulseuji/An-Optimized-BP-Neural-Network-Model-Based-on-Genetic-Algorithm-for-Human-Pre-miRNA-Classification/blob/main/GA-BPNN_Codes_and_Plots.ipynb)


也是自己最近要打比赛又翻出来这个项目才想起来给它加一个readme 

当时还是小白可能有很多不足的地方 所以也欢迎大家批评指正 

最后希望大家都能拿一个好成绩！

<div align=center>
<img src="https://github.com/user-attachments/assets/6917e50e-6767-4661-8dbb-6eb0cdb51f93" width="70" height="60" />
</div>

---

### 上面那份Notebook里所建立的 GA-BPNN 模型的参数与架构如下
### 一些选择上的细节 还有参数对应的意义 文章里都有相应解释

#### 网络架构
- 输入层：42 个特征（选择后得到的来自人类前体miRNA的序列和结构特征）
- 隐藏层：1 个隐藏层 神经元数为 12（由实验优化得到）
- 输出层：2 个节点（对应两种待划分的类别）


#### 网络参数

- 激活函数：Sigmoid
- 学习率：0.05
- 最大迭代次数：1000
- 目标误差：1e-5

#### 遗传算法参数
- 种群规模：20
- 最大进化代数：200
- 交叉概率：0.4
- 变异概率：0.1
- 适应度函数：均方误差 (MSE)

#### 总结
- 文章的 GA-BPNN 架构是： 42-12-2 的三层网络 + 采用遗传算法优化各层间的权重和阈值（注意不是优化架构的层数和节点数）
- 最终模型性能用 Accuracy + Sensitivity + Specificity + Precision + F1-score + MCC + ROC/AUC 全面评估


