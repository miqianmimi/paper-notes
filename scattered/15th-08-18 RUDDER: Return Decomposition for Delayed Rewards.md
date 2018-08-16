# RUDDER: Return Decomposition for Delayed Rewards
`Jose A.Arjona-Medina`-`LIT AI Lab`-`Johannes Kepler University Linz, Austria`

## Abstract 
> ### What we do
> 
> We propose a noevle reinforcement learning approach for finite Markov Decision processes(MDPs) with delayed rewards.
> 
> Furthermore variances of Monte Carlo(MC) estimates are proved to increase the variance of other estimates, the number of which can ecponentially grow in the number of delay steps. 
> 
> We introduce `RUDDER`, a return decomposition method, which creats a new MDP with same optimal policies as the orignal MDP, but with redistributed rewards that largely reduced delays.
> 
> MDP does not have delayed rewards and TD(temporal difference) estimates are unbiased. 
> 
> `RUDDER`  is exponentially faster than `TD`,`MC`, and `MC Tree Search(MCTS)`. Also, It outperforms `rainbow`, `A3C`, `DDQN`, `Distributional DQN`, `Dueling DDQN`, `Noisy DQN`, and `Prioritized DDQN` on the delayed reward Atari game Venture in only a fraction of the learning time.

---

## 2.Introduction

> ### Recent Works:
> Distributional Q-learning profits from noise since means that have high variance are more likely selected.
> 
> `LSTM` was already used in reinforcement learning for advantage learning. However, this has major drawbacks.
> 
> We propose  `RUDDER`, which performs reward redistribution by return decomposition and , therefore overcomes problems of TD and MC stemming from delayed rewards.
> 
---
 


## 3.Return Decomposition and Reward Redistribution

> `Bias-Variance for MDP Estimates`
> 
> `Delayed Reward Aggravates Learning`

> RUDDER "Return decomposition for Delayed Rewards ", which performs return decomposition using a long short-term memory(LSTM) network for redistributing the orignal reward.
> 
> * (1) Safe expokartion
> 
> * (2) Lessons replay buffer
>  
> * (3) LSTM and contribution analysis

 ---
 

## 4.Conclusion:

> `Exploration` 
> 
> is most critical, since discovering delayed rewards is the first step to exploit them.
> 
> `Human expert episode` 
> 
> are an alternative to exploration and can serve to fill the lessons replay buffer. Learning can be sped up considerably when LSTM identifies human key actions. Return decomposition will reward human key actions even for episodes with low return since other actions that thwart high returns receive negative reward. 
> 
> `Conclusion` 
> 
> We have shown that for finite Markov decision processes with delayed rewards TD exponentially slowly corrects biases and MC can increase many varianves of estimates exponentially, both in the number of delay steps.
>  
> We have introduced RUDDER, **a return decomposition method**, which creats a new MDP that keeps the optimal policies but its redistributed rewards do not have delays. 
