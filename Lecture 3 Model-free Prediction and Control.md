# Lecture 3: Model-free Prediction and Control

### Model-Free RL:

Model-free: solve an **unknown** MDP

In a lot of real-world problems, MDP model is either unknown or known by too big or too complex to use

* Atari Game, Game of Go, Helicopter, Portfolio management, etc

Model-free RL can solve the problems through interaction with the environment<img src="https://i.loli.net/2020/03/30/OdR3J9Ha7yoGKNX.png" alt="截屏2020-03-30 10.29.14" style="zoom:50%;" />

How to do policy evaluation:

* Monte Carlo policy evaluation（采样）
* Temporal Difference (TD) learning

###Monte Carlo policy evaluation 

![截屏2020-03-30 10.33.01](https://i.loli.net/2020/03/30/CeV1SjDQIT8kKis.png)

更方便的方法：

<img src="https://i.loli.net/2020/03/30/Jjai9OsXdr4PVuq.png" alt="截屏2020-03-30 10.35.09" style="zoom: 25%;" />

#### MC & DP

MC --> model free，DP --> require MDP

MC --> fast

### Temporal Difference (TD) learning

TD learns from incomplete episodes, by bootstrapping

### DP，MC，TD的区别

#### DP

![截屏2020-03-30 10.49.13](https://i.loli.net/2020/03/30/iTdyESaoUxbkqZI.png)

#### MC

![截屏2020-03-30 10.49.25](https://i.loli.net/2020/03/30/zjLt3CpqEgRFdBn.png)

#### TD

![截屏2020-03-30 10.50.19](https://i.loli.net/2020/03/30/5IJwHyDXxc3uiMT.png)

#### 综合比较

![截屏2020-03-30 10.51.05](https://i.loli.net/2020/03/30/Lztlrfp3u4PsjBX.png)

### Model-free Control for MDP

#### $\epsilon-Greedy$: ensure exploration

![截屏2020-03-30 11.02.07](https://i.loli.net/2020/03/30/v2bxWXPMGmjcYfO.png)

#### Monte Carlo with ε-Greedy Exploration

![截屏2020-03-30 11.02.58](https://i.loli.net/2020/03/30/EWT2zdUa3YuqC7N.png)

### On-policy learning & Off-policy learning

On-policy: 使用一个策略进行探索/学习

![截屏2020-03-30 11.09.23](https://i.loli.net/2020/03/30/IXemhFQrC6b3Ktu.png)

### Q learning

![截屏2020-03-30 11.20.14](https://i.loli.net/2020/03/30/iBZX8LWRTDeEHo5.png)

