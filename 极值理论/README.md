## 极值理论
### 参考资料
https://www.youtube.com/watch?v=IiOSxaF5oxo
https://www.zybuluo.com/fanxy/note/397826#2-var%E8%AE%A1%E7%AE%97%E7%9A%84%E8%AE%A1%E9%87%8F%E7%BB%8F%E6%B5%8E%E5%AD%A6%E6%96%B9%E6%B3%95

### 两种分析方法
1. Annual Maxima Series（找每一块的最大值（最小值））
2. Peak Over Threshold（设置threshold）
极端数据的采集方式不同，在此基础上拟合的分布类型也不同。
POT方法采集的数据，用Generalized Pareto Distribution（广义帕累托分布）进行拟合； 
BM方法采集的数据，用Generalized Extreme Value分布来拟合。

#### Threshold exceedances
从论文"Anomaly Detection in Streams with Extreme Value Theory"中第一次看到极值理论。
简单来说，极值理论出现是因为人们发现正态分布等常见分布不能很好地拟合极端数据的分布。
所以，数学家创造了另一种分布来拟合极端数据，BM采样方法出现的早一些，但是目前POT采样似乎用得更多。
基于POT采样出来的数据，我们认为其服从广义帕累托分布。
那么如果我们想知道具体的分布函数，我们要对分布中的shape和scale参数进行估计，这就引出了极大似然估计。
在"Anomaly Detection in Streams with Extreme Value Theory"中，作者还提到Grimshaw's trick对极大似然估计进行reduction。
分布函数出来了以后，就想干嘛干嘛了。
