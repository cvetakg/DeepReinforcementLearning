Author: Jelena Kocic, July 2018.

*Learning resources: RL Course by David Silver-DeepMind, Udacity-DRLND, arXiv, booxs and many others*

# Deep Reinforcement Learning


## 1. Introduction

Reinforcement Learning is a form of learning in which a software agent observes the environment and takes actions to maximize its rewards from the environment.

![](RL.png)

Machine learning paradigms:
- Supervised Learning: y=f(x)
- Unsupervised Learning: f(x)
- Reinforcement Learning: y=f(x), z

#### Reinforcement Learning vs Supervised Learning

Reinforcement learning is different from supervised learning in the sense that there are no labels in advance to tune the parameters of the model. The model learns from the rewards received from the runs. Although the short-term rewards are available instantly, long-term rewards are only available after a couple of steps. This is also known as delayed feedback.

#### Reinforcement Learning vs Unsupervised Learning

Reinforcement learning is also different from unsupervised learning because in unsupervised learning there are no labels available, whereas in reinforcement learning the feedback is available in terms of the rewards.

Unsupervised learning mainly deals with finding structure in data.

Reinforcement learning use an agent that knows if a move is good or bad, by the reward it gets. A bad action in a particular state will have less reward than a good action. 

Reinforcement learning is different from unsupervised learning, which is typically about finding structure hidden in collections of unlabeled data. The terms supervised learning and unsupervised learning would seem to exhaustively classify machine learning paradigms, but they do not. *Although one might be tempted to think of reinforcement learning as a kind of unsupervised learning because it does not rely on examples of correct behavior, reinforcement learning is trying to maximize a reward signal instead of trying to find hidden structure.* Uncovering structure in an agent's experience can certainly be useful in reinforcement learning, but by itself does not address the reinforcement learning problem of maximizing a reward signal. We therefore consider reinforcement learning to be a third machine learning paradigm, alongside supervised learning and unsupervised learning and perhaps other paradigms.


#### Introduction to Deep Reinforcement Learning- The RL Framework

Interpret the Policy
A policy determines how an agent chooses an action in response to the current state. In other words, it specifies how the agent responds to situations that the environment has presented.


### Documentary, Videos 

[AlphaGo - The Movie](https://www.youtube.com/watch?v=WXuK6gekU1Y&t) (Full Documentary)

[Introduction to Reinforcement learning with David Silver](https://www.youtube.com/watch?v=2pWv7GOvuf0&list=PLqYmG7hTraZBiG_XpjnPrSNw-1XQaM_gB) (DeepMind), [slides](https://www.davidsilver.uk/teaching/)



## 2. Reinforcement Learning - Intro


### 2.1. Introduction to Reinforcement Learning

![](img/rl6.PNG)

What makes reinforcement learning different from other machine learning paradigms?
- There is no supervisor, only a reward signal
- Feedback is delayed, not instantaneous
- Time really matters (sequential, non i.i.d data)
- Agent's actions affect the subsequent data it receives

![](img/rl7.PNG)

History and State
- The history is the sequence of observations, actions, rewards
Ht = O1, R1, A1, ..., At-1, Ot , Rt
- i.e. all observable variables up to time t
- i.e. the sensorimotor stream of a robot or embodied agent
- What happens next depends on the history:
- *The agent selects actions*
- *The environment selects observations/rewards*
- State is the information used to determine what happens next
- Formally, state is a function of the history:

St = f (Ht )

![](img/rl8.PNG)
![](img/rl9.PNG)
![](img/rl10.PNG)

An RL agent may include one or more of these components:
- **Policy**: agent's behaviour function
- **Value function**: how good is each state and/or action
- **Model**: agent's representation of the environment

![](img/rl11.PNG)
![](img/rl12.PNG)
![](img/rl13.PNG)
![](img/rl14.PNG)
![](img/rl15.PNG)
![](img/rl16.PNG)

**Exploration and Exploitation**

- Reinforcement learning is like trial-and-error learning
- The agent should discover a good policy
- From its experiences of the environment
- Without losing too much reward along the way
- *Exploration* finds more information about the environment
- *Exploitation* exploits known information to maximise reward
- It is usually important to explore as well as exploit

**Prediction**: evaluate the future
- Given a policy

**Control**: optimise the future
- Find the best policy

### 2.2. Markov Decision Process



### 2.3. Planning by Dynamic Programming



### 2.4. Model-Free Prediction


### 2.5. Model Free Control



### 2.6. Value Function Approximation


### 2.7. Policy Gradient Methods



### 2.8. Integrating Learning and Planning



### 2.9. Exploration and Exploitation


### 2.10. Classic Games



## 3. Deep Reinforcement Learning

### 3.1. Foundations of RL
*(Classical RL problems)*

### 3.2. Value-Based Methods

#### Navigation
*(Use NN to train an agent that learns intelligent behaviors from sensory data.)*

### 3.3. Policy-Based Methods

#### Continuous Control
*(Train a robotic arm to reach target locations, or train a four-legged virtual creature to walk.)*


### 3.4. Multi-Agent Reinforcement Learning

#### Collaboration and Competition
*(Train a system of agents to demonstrate collaboration or cooperation on a complex task.)*

Multi-agent communication:

Communication lats the foundation for multi-agent cooperation, e.g.:
- Intelligent Transportation Systems
- Autonomous Driving
- Moba Game

![](rl1.PNG)

## Papers

### 4.1. Reinforcement Learning with Augmented Data, [link](https://arxiv.org/abs/2004.14990)

#### Michael Laskin, Kimin Lee et al., NIPS2020

![Different types of data augmentations](rl2.PNG)

![](rl3.PNG)

![](rl4.PNG)

#### Data-efficiency when learning from pixels

Simple RL with data aug, outperforms prior state-of-the-art methods on DeepMind Control.

RL with data ugmentation implicitly learns better features:
1. Data augs help ConvNet focus on important visual features
2. Random crom/translate make the biggest difference

Specifically, translation augmentation plays the most important role. 

#### Generalization when learning from pixels

Data augmentation significantly improves PPO generalization on ProcGen environments

![](rl5.PNG)

#### Data-efficiency when learning from state

RAD (Reinforcement Learning with Augmented Data) is competetive with more complex state-based RL methods despite its simplicity

#### Takeaway: Simple RL + data augmentation provides a powerful baseline for both pixel and state-based RL
