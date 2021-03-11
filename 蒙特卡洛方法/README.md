 ## 
 # 第五章 蒙特卡洛方法
 
本章主要介绍蒙特卡洛方法。蒙特卡洛方法从经验中学习，无需对环境有完全的了解。

1. 预测

```
First-visit MC prediction, for estimating V ≈ v_pi

Input: a policy pi to be evaluated
Initialize:
    V(s) ∈ R, arbitrarily, for all s ∈ S
    Returns(s) <- an empty list, for all s ∈ S

Loop forever (for each episode):
    Generate an episode following pi: S_0, A_0, R_1, S_1, A_1, R_2,...,S_T-1,A_T-1, R_T
    G <- 0
    Loop for each step of episode, t = T-1, T-2,...,0:
        G <- G + R_t+1
        Unless S_t appears in S_0, S_1,...,S_t-1:
            Append G to Returns(S_t)
            V(S_t) <- average(Returns(S_t))
```
            
以上是首次访问蒙特卡洛法，只取状态序列中特定状态第一次出现的收获值；而每次访问蒙特卡洛法取特定状态每次出现的收获值。

2. 控制


## 本节目录
1.[习题解答](习题解答.md)
