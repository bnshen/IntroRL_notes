# Lec 5: Policy Optimization I

### Value-based RL versus Policy-based RL

![截屏2020-04-17 13.01.38](https://i.loli.net/2020/04/17/EAMqa1hPHjVXZbm.png)

### Policy-based RL的优势

![截屏2020-04-17 13.03.43](https://i.loli.net/2020/04/17/2XCgyN5tBpDYQzV.png)

#### Two types of policies:

* Deterministic
* Stochastic 

value-based RL learns a deterministic policy

<img src="https://i.loli.net/2020/04/17/h1nk2XLBReCTYqO.png" alt="截屏2020-04-17 13.09.34" style="zoom:25%;" />

Policy-based RL can learn the optimal stochastic policy

<img src="https://i.loli.net/2020/04/17/K1Zb7jBAa3mIRsO.png" alt="截屏2020-04-17 13.09.41" style="zoom:25%;" />

原因在于policy-based RL输出概率

policy-based RL目的在于极大化随机采样的奖励

<img src="https://i.loli.net/2020/04/17/RJfUgc7WOZYSLn5.png" alt="截屏2020-04-17 13.13.49" style="zoom:33%;" />

### 优化方法

* 可导：
  * Gradient accend
* 不可导: 
  * Cross-Entrophy：每次取前10%，让总体分布接近这10%(argmax)
  * Finite Difference：加$\epsilon$的扰动，算出梯度的近似



* score function
  * 使得 Policy Gradient 的优化与dynamic transition无关
  * 使用蒙特卡洛的方法来计算gradient

* 鼓励policy获得更高的分数

<img src="https://i.loli.net/2020/04/17/UCWbF8XAl3ESvHB.png" alt="截屏2020-04-17 14.09.40" style="zoom:25%;" />

#### m-c方法的优缺点

* Unbiased but very noisy

* 解决方法：
  * Use temporal causality，与后期采取的动作无关
  * Use a baseline，$G_{t} \Longrightarrow (G_{t} - b(s_{t}))$，Variance降低

但是$G(t)$其实是采样得到的，于是可以直接近似估计$G(t)$，于是引入critic

### Actor-Critic Policy Gradient

![截屏2020-04-17 14.21.08](https://i.loli.net/2020/04/17/HUVugKPRambtJ9G.png)

#### 优化

![截屏2020-04-17 14.23.16](https://i.loli.net/2020/04/17/ENMXxhnFYLJgve6.png)

然后可以使用神经网络代替Actor和Critic

#### Extension

* A2C, A3C
* TRPO
* PPO

