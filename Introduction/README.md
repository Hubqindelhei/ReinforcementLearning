## Introduction to Reinforcement Learning

###### What makes reinforcement learning different from other machine learning paradigms?
- There is no supervisor, only a reward signal
- Feedback is delayed, not instantaneous
- Time really matters (sequential)
- Agent's actions affect the subsequent data it receives

###### Rewards
- A reward is a scalar feedback signal
- Indicate how well agent is doing at step t
- The agent's job is to maximise cumulative reward

###### Sequential Decision Making
- Goal: select actions to maximise total future reward
- Actions may have long term consequences
- Reward may be delayed
- It may be better to sacrifice immediate reward to gain more long-term reward

###### History and State
- The history is the sequence of observations, actions, rewards
&emsp;&emsp;&emsp;&emsp; Ht = O1,R1,A1,...,At-1,Ot,Rt
- State is the information used to determine what happens next
&emsp;&emsp;&emsp;&emsp;St = f(Ht)

###### Environment State
- pick next observation / reward
- not usually visible to the agent
- even if visible, it may contain irrelevant information

###### Agent State
- pick next action
- it is the information used by reinforcement learning algorithms
- it can be any function of history

###### Information State
- A state St is Markov if and only if
&emsp;&emsp;&emsp;&emsp; P[St+1 | St] = P[St+1 | S1,...,St]
- Once the state is known, the history may be thrown away

###### Full observability: agent directly observes environment state
- agent state = environment state = information state
- this is a Markov decision process (MDP)

###### Partially Observable Environments
- agent indirectly observes environment
- agent state != environment state
- this is a Partially Observable Markov decision process (POMDP)

###### Major Components of an RL Agent
- Policy: agent's behaviour function
- Value function: how good is each state and / or action
- Model: agent's representation of the environment

###### Policy
- A policy is the agent's behaviour
- It is a map from state to action

###### Value function
- Value function is a prediction of future reward
- Used to evaluate the goodness/badness of states

###### Model
- model predicts what the environment will do next

###### Exploration and Exploitation  
- Exploration finds more information about the environment
- Exploitation exploits known information to maximise reward
- It is usually important to explore as well as exploit


### References
- [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/bookdraft2018jan1.pdf) - Chapter 1: The Reinforcement Learning Problem
- David Silver's RL Course Lecture 1 - Introduction to Reinforcement Learning ([video](https://www.youtube.com/watch?v=2pWv7GOvuf0), [slides](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching_files/intro_RL.pdf))

