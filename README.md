# 机器学习(Machine Learning)
- 监督学习(Supervised Learning)：训练样本带有信息标记(**y值**)，利用已有的训练样本信息学习数据的规律预测未知的新样本标签。
  - 回归分析(Regression)
  - 分类(Classification)
- 无监督学习(Unsupervised Learning)：训练样本的标记信息时未知的，目测是为了揭露训练样本的内在数学，结构和信息，为进一步的数据挖掘提供基础。
  - 聚类(Clustering)
## 回归
- 

## 分类算法
- 一种对**离散型随机变量**建模或预测的监督学习算法。
- 使用案例包括邮件过滤、金融欺诈和预测雇员异动等输出为类别的任务。
- 分类算法通常适用于预测一个类别(或类别的概率)而不是连续的数值。

### (基础)决策树 Decision Tree
决策树是一个树结构(可以是二叉树或非二叉树)。

其每个非叶节点表示一个**特征属性**上的测试，每个分支代表这个特征属性在某个值域上的输出，而每个叶节点存放一个类别。

使用决策树进行决策的过程就是从**根节点开始**,测试待分类项中相应的特征属性，并按照其值选择输出分支，知道到达叶子节点，将**叶子节点**存放的类别作为决策结果。

**优点：**
- 适用任何类型的数据(类别变量更普遍)
- 直观、决策树可以提供可视化，便于理解
- 模型预测出的结果简单，可解释性强
- 适用于小规模数据

**缺点：**
- 当数据中存在连续变量的属性时，决策树表现并不是很好
- 不稳定性，一点点的扰动或者改动都可能改动整棵树
- 特殊属性增加时，错误增加的比较快
- 很容易在训练数据中生成复杂的树结构，造成过拟合。

### 随机森林 Random Forest
![image](https://github.com/teamowu/Machine-Learning/blob/master/images/Random%20Forest.png)

**优点：**
- 随机森林不容易限于过拟合
- 具有很好的抗噪声能力
- 处理很高维度(feature多)的数据，并且不用做特征选择
- 训练速度快

## 聚类
- 一种无监督式机器学习(即**数据没有标注**)
- 算法基于数据的内部结构寻找观察样本的自然族群(即集群)
- 使用案例包括客户细分，新闻聚类，文章推荐等等。

**用于衡量相似性的几个指标**：
- 欧式距离 Euclidean distance
  - 定义：指在m维空间中两个点之间的真实距离，或者向量的自然长度（即该点到原点的距离）
  - 用途：
  
![image](https://github.com/teamowu/Machine-Learning/blob/master/images/%E6%AC%A7%E5%BC%8F%E8%B7%9D%E7%A6%BB.png)

- 曼哈顿距离 Manhattan distance
  - 定义：就是表示两个点在标准坐标系上的绝对轴距之和。
  - 用途：
  
![image](https://github.com/teamowu/Machine-Learning/blob/master/images/%E6%9B%BC%E5%93%88%E9%A1%BF%E8%B7%9D%E7%A6%BB.png)

- 余弦相似性 cosine
  - 定义：通过计算两个向量的夹角余弦值来评估他们的相似度。
  - 用途：新闻分类
  
![image](https://github.com/teamowu/Machine-Learning/blob/master/images/%E4%BD%99%E5%BC%A6%E7%9B%B8%E4%BC%BC%E6%80%A7.png)

- Jaccard系数
  - 定义：给定两个集合A,B，Jaccard 系数定义为A与B交集的大小与A与B并集的大小的比值。
  - 用途：用于比较有限样本集之间的相似性与差异性。Jaccard系数值越大，样本相似度越高。
  
![image](https://github.com/teamowu/Machine-Learning/blob/master/images/jaccard%E7%B3%BB%E6%95%B0.png)

### 层次聚类 Hierarchical Cluster Analysis(HCA)
层次聚类是一系列基于以下概念的聚类算法：
- 最开始由一个数据点作为一个集群
- 对于每个集群，基于相同的标准合并集群
- 重复这一过程直到只留下一个集群，因此就得到了集群的层次结构。

### K均值聚类 K-means Clustering Algorithm
- 聚类的度量基于样本点之间的几何距离(即在坐标平面中的距离)
- 集群是围绕在聚类中心的族群，而集群呈现出类球状并具有相似的大小
- 对于给定的k值，算法先给出一个初始的分组方法，然后通过反复迭代的方法改变分组，使得每一次改进之后的分组方案较前一次好

### DBSCAN
- 基于密度的算法，它将样本点的密度区域组成一个集群
- DBSCAN不需要假设集群为球状，并且它的性能是可拓展的
- 不需要每个点都被分配到一个集群中，这降低了集群的异常数据。
  
## 降维

## 离群值检测
