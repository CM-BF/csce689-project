# CSCE689 project


## Introduction

In traditional machine learning, it is generally assumed that training and test data are i.i.d.. However, in the common case where the i.i.d. assumption does not hold, model performance could experience significant drops during test period. Out-of-distribution (OOD) learning focuses on scenarios where the training distribution is different from test distribution. The omnipresence of the OOD problem across all machine learning fields makes OOD generalization a critical area of research, which also applies for reinforcement learning studies. 
Reinforcement learning (RL) provides a powerful framework that can train an agent to take proper sequential actions based on the states. To apply RL models in reality without significant OOD performance drop, we expect to generalize the agents trained in training environments to unseen testing environments. OOD generalization in RL is only an emerging area of research, and many existing works make use of extra data from the testing environments. Since the testing distribution is commonly unknown in real-world applications, an effective generalizable policy that only accesses data from training environments is urgently needed. 

One of the solutions for the OOD problem is to discover the factors of variation that affect the environmental dynamics, from which a generalizable policy can be learned.


## Experiments

In reinforcement learning, the main experiment can be run in `reinforcement_learning` directory with
```
MUJOCO_GL=egl DOMAIN=cartpole TASK=swingup SAVEDIR=./save CUDA_VISIBLE_DEVICES=0 python train.py env=cartpole_swingup experiment=cartpole_swingup agent=vrex seed=1 agent.params.penalty_weight=1
```
