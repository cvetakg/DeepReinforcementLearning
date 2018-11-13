Jelena Kocic, July 2018.

# Deep Reinforcement Learning

### Content:

1. Introduction 
2. Value-Based Models
3. Policy-Based Methods
4. Multi-Agent Reinforcement Learning



## Introduction

Reinforcement Learning is a form of learning in which a software agent observes the environment and takes actions to maximize its rewards from the environment.

![](RL.png)

Machine learning paradigms:
- Supervised Learning
- Unsupervised Learning
- Reinforcement Learning

#### Reinforcement Learning vs Supervised Learning

Reinforcement learning is different from supervised learning in the sense that there are no labels in advance to tune the parameters of the model. The model learns from the rewards received from the runs. Although the short-term rewards are available instantly, long-term rewards are only available after a couple of steps. This is also known as delayed feedback.

#### Reinforcement Learning vs Unsupervised Learning

Reinforcement learning is also different from unsupervised learning because in unsupervised learning there are no labels available, whereas in reinforcement learning the feedback is available in terms of the rewards.

Unsupervised learning mainly deals with finding structure in data.

Reinforcement learning use an agent that knows if a move is good or bad, by the reward it gets. A bad action in a particular state will have less reward than a good action. 

Reinforcement learning is different from unsupervised learning, which is typically about finding structure hidden in collections of unlabeled data. The terms supervised learning and unsupervised learning would seem to exhaustively classify machine learning paradigms, but they do not. Although one might be tempted to think of reinforcement learning as a kind of unsupervised learning because it does not rely on examples of correct behavior, reinforcement learning is trying to maximize a reward signal instead of trying to find hidden structure. Uncovering structure in an agent's experience can certainly be useful in reinforcement learning, but by itself does not address the reinforcement learning problem of maximizing a reward signal. We therefore consider reinforcement learning to be a third machine learning paradigm, alongside supervised learning and unsupervised learning and perhaps other paradigms.



### 1. Introduction to Deep Reinforcement Learning


#### 1.1. The RL Framework

Interpret the Policy
A policy determines how an agent chooses an action in response to the current state. In other words, it specifies how the agent responds to situations that the environment has presented.
