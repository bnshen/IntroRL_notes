#Lecture 4: Value Function Approximation

### RL从小规模到大规模

* 状态数指数级增长

![截屏2020-04-06 11.12.20](https://i.loli.net/2020/04/06/lf2WaXLk3Us9uni.png)

* 少量状态可以用`lookup table`来表示特征，大量状态无法装入内存，同时无法学习如此大量的状态

### 函数近似

* 避免明确学习每一个状态

  <img src="https://i.loli.net/2020/04/06/reICigDKycXhOmq.png" alt="截屏2020-04-06 11.14.47" style="zoom: 50%;" />

* 通过已见到的状态估计未见到的状态

#### 函数近似的几种情况

* 线性拟合【可微分】-->【梯度下降】
* 神经网络【可微分】-->【梯度下降】
* 决策树
* K近邻

#### 梯度下降

* 在线性拟合的情况下`局部最优`自动成为`全局最优`

### Model-free情况下value函数近似

* 没有ground truth，只有rewards

<img src="https://i.loli.net/2020/04/06/KdQ87iqWUzykjAg.png" alt="截屏2020-04-06 11.26.40" style="zoom:50%;" />

### 强化学习中的不稳定因素

* 近似函数：引入误差
* bootstrapping：根据先前的经验估计而不是完全依赖新的reward
* off-policy：训练用函数和实际update的函数不同

### Why deep neural networks

* 自动提取特征
* 非线性函数拟合

### Deep Q-Networks

####  优化方法

<img src="https://i.loli.net/2020/04/06/gXclRjsvnL16QM5.png" alt="截屏2020-04-06 12.01.55" style="zoom:67%;" />

* experience replay

  * <img src="https://i.loli.net/2020/04/06/NyYMeWrdvVakp15.png" alt="截屏2020-04-06 12.05.22" style="zoom:67%;" />

* fixed targets

  * 改善稳定性
  * <img src="https://i.loli.net/2020/04/06/SJMNAbIEVX71f2z.png" alt="截屏2020-04-06 12.09.28" style="zoom:67%;" />

  #### Abalation Study

![截屏2020-04-06 12.11.03](https://i.loli.net/2020/04/06/HvbhiLOUPuMGfwC.png)

#### DQN 总结

![截屏2020-04-06 12.17.35](https://i.loli.net/2020/04/06/z3AaYTyDMxflrQe.png)

