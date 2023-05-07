# Reinforcement_Learning_Lecture_Notes 


## Overview: Value Network vs Policy Network
Value Network examples: Q-learning, DQN(The agent's brain in Q-learning is the Q-table, but in DQN the agent's brain is a deep neural network), SARSA[on-policy]

Policy Network examples: REINFORCE (Monte Carlo)[on-policy], Actor-Critic, TRPO (clip gradients), PPO  (clip gradients), DPG (Continuous control, two deterministic policy network, one for mean value of continous actions, the other for variance, ), DDPG


### Dynamic Programming vs Monte Carlo simulations vs Temperal Difference 
Those are 3 ways to utilize the detected rewards to guess unknown values. Only we have the value model, we can optimize our behaviors/actions. 


#### Dynamic prgramming summary
It requies the full knowledge of transition probility matrix, which is the probility from state s to all the posible states s', so that it can average all the possible returns, as showed below. 

![image](https://user-images.githubusercontent.com/91216581/232410332-c939bd56-5f05-41b0-bceb-ab771e99b966.png)

![image](https://user-images.githubusercontent.com/91216581/206213936-43cf218f-e40f-4d46-8dff-90b8db5a0285.png)


#### Monte Carlo summary
However, the monte carlo only needs to sample the average future return of state s under sample trajectories from past experience. 

![image](https://user-images.githubusercontent.com/91216581/206213954-02652d2d-4ec5-4832-afcb-32e268d3e30b.png)

### TD Algorithm summary
TD tends to reduce the estimation error of value along the attempts. It's more intuitive, since we can't forsee the end of the story in most cases, and the way we learn is to get the feedbacks from the world and modify our value table knowleadges. 

![Screenshot 2022-12-07 at 16 59 17](https://user-images.githubusercontent.com/91216581/206228142-c93da78c-b605-4f6a-88eb-d029c4bae18f.png)

![image](https://user-images.githubusercontent.com/91216581/206213963-91a8a3e6-0f1d-445e-bbd1-f9c30a5cfb16.png)


## Algorithms' sudo code
### Q-learning (offline)

reference: https://zhuanlan.zhihu.com/p/81437177

![image](https://user-images.githubusercontent.com/91216581/232432841-66ab71da-897b-4668-9451-8e910f021b6b.png)

### Sarsa (online)


![image](https://user-images.githubusercontent.com/91216581/232432883-6a76aeab-cbd0-4e7f-8cc2-1c43e9f9b215.png)



### DQN (offline)

The agent's brain in Q-learning is the Q-table, but in DQN the agent's brain is a deep neural network

![image](https://user-images.githubusercontent.com/91216581/236658180-7b0e0a28-db37-4acb-ab68-1fe7d46cccfc.png)

<img width="474" alt="image" src="https://user-images.githubusercontent.com/91216581/236658197-447135a1-92e1-4c12-a865-b80e3946416a.png">


