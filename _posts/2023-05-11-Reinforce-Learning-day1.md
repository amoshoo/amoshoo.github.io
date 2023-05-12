---
layout: post
title:  "Math foundation for RL day1"
date:   2023-5-11 10:00:40
blurb: "A study markdown for math foundation of reinforce learning, according to lecture by Prof. Shiyu Zhao, Westlake University"
og_image: /assets/img/content/post-example/Banner.jpg
---

<img src="{{ "/assets/img/content/post-example/Banner.jpg" | absolute_url }}" alt="bay" class="post-pic"/>
<br />
<br />

Picture by [Bethany Legg](https://unsplash.com/@bkotynski).
Day 1 for reinforce learning[^1]

Related book
1. Sutton, Richard S., and Andrew G. Barto. Reinforcement learning: An introduction. MIT press, 2018. (most classic, but not for layman)

<br />


#### Table of Contents
1. [Before Class](#before-class)
2. [Basic Concepts](#basic-concepts)
    * [Basic Elements](#basic-elements)
    * [Markov Decision PROCESS](#markov-decision-process)
3. [Footnotes](#footnotes)

#### BEFORE CLASS
Features of RL
* More mathematical
* Systematic
<br />

Arrange suitable time for your study!

Brief Intro to History
* Story of Alpha GO
* AlphaGo Zero vs AlphaGo
* Deep Q Learning (Watkins)
* More History...

<br />
<br />

#### BASIC CONCEPTS
Here we first describe some basic concepts in reinforcement learning, take grid of cell as example, we need to find a good path from start to target.

<br />

##### BASIC ELEMENTS
* state: the status of the agent with respect to the environment, in the above example, the location of the agent is the state. All of states consist of the state space $$S = \{s_{i}\}, i = 1,2,...,9$$
* action: for each state, we have corresponding actions, all of actions consist of action space. $$A(s_{i})=\{a_{i}\}$$
* state transition: after taking an action, the agent may move from one state to another, which define the interaction with the environments. $$s_{1} \rightarrow s_{2}$$
* forbidden area: accessible (but with penalty); inaccessible
* tabular representation: used to describe the state transition
* state transition probability: $$p(s_{2}\|s_{1},a_{2})=1$$
* policy: policy tells the agent what actions to take at a state. e.g. $$\pi (a_{1}\|s_{1})=0$$, which can be represented by tabular representation
* reward: a real number we get after taking an action. Reward can be interpreted as a human-machine interface, with which we can guide the agent to behave as what we expect. we can use tabular representation to represent the reward. $$p(r=-1\|s_{1},a_{1})=1$$
* reward depends on the  state and the action, but not the next state.
* trajectory: a state-action-reward chain
* return: the sum of all the rewards collected along the trajectory
* discounted return: after introduce the discounted rate $$\gamma \in [0,1)$$, we could prevent the return diverging. we could change the discount rate to make the policy favor the near future reward(small $$\gamma$$） or the far future reward(big $$\gamma$$)
* episode: when interacting with the environment following a policy, the agent may stop at some terminal states, the resulting trajectory is called an episode(or an trial). Some tasks may have no terminal states, meaning the interaction with environments will never end, such a task are called continuing tasks.

<br />

##### MORKOV DECISION PROCESS
Markov Decision Process(MDP), key element of MDP includes
* Sets: the set of states, the set of action, the set of reward
* probability distribution: state transition probability, reward probability
* Policy: at state $$s$$, the probability to choose action $$a$$ is $$\pi (a\|s)$$
* Markov property: memoryless property

<br />


##### FOOTNOTES

[^1]: This is a note!

