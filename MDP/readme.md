## Markov Decision Processes
Markov decision processes formally describe an environment for reinforcement learning, where the environment is fully observable. 



#### 1. Markov Process
A Markov process is a memoryless random process, i.e. a sequence of random states S1, S2,.. with the Markov property 
```
Definition

A Markov Process (or Markov Chain) is a tuple ⟨S,P⟩
- S is a finite set of states
- P is a state transition probability matrix,
    Pss' = P [St+1 = s' | St = s]
```

#### 2. Markov Reward Processes

A Markov reward process is a Markov chain with values.
```
Definition

A Markov Reward Process is a tuple <S, P, R, r>
- S is a finite set of states
- P is a state transition probability matrix,
    Pss' = P [St+1 = s' | St = s]
* R is a reward function, Rs = E[ Rt+1 | St = s ]
* r is a discount factor, 0 <= r <= 1
```

##### Return
Total discounted reward from time-step t.

<div align="center">
<img src="http://latex.codecogs.com/gif.latex?G_%7Bt%7D%20%3D%20R_%7Bt&plus;1%7D%20&plus;%20%5Cgamma%20R_%7Bt&plus;2%7D%20&plus;%20...%20%3D%20%5Csum_%7Bk%3D0%7D%5E%7B%5Cinfty%7D%5Cgamma%20%5E%7Bk%7D%20R_%7Bt&plus;k&plus;1%7D">
</div>

##### Value function
Expected Return starting from state s.
<div align="center">
<img src="http://latex.codecogs.com/gif.latex?v%28s%29%20%3D%20E%20%5B%20G_%7Bt%7D%20%7C%20S_%7Bt%7D%3Ds%20%5D">
</div>


#### 3. Markov Decision Processes
A Markov decision process(MDP) is a Markov reward process with decisions.
```
Definition
A Markov Decision Process is a tuple<S,A,P,R,r>
- S is a finite set of states
* A is a finite set of actions 
- P is a state transition probability matrix
- R is a reward function
- r is a discount facter
```
<div align="center">
<img src="http://latex.codecogs.com/gif.latex?P_%7Bss%27%7D%5E%7Ba%7D%20%3D%20P%20%5B%20S_%7Bt&plus;1%7D%20%3D%20s%27%20%7C%20S_%7Bt%7D%3Ds%2C%20A_%7Bt%7D%3Da%5D%5C%5C">
</div>

<div align="center">
<img src="http://latex.codecogs.com/gif.latex?R_%7Bs%7D%5E%7Ba%7D%20%3D%20E%5BR_%7Bt&plus;1%7D%20%7C%20S_%7Bt%7D%3Ds%2CA_%7Bt%7D%3Da%5D">
</div>

##### Policies
A policy is a distribution over actions given states.
<div align="center">
<img src="http://latex.codecogs.com/gif.latex?%5Cpi%20%28a%20%7C%20s%29%20%3D%20P%20%5BA_%7Bt%7D%20%3D%20a%20%7C%20S_%7Bt%7D%20%3D%20s%5D">
</div>
- A policy fully defines the behaviour of an agent
- MDP policies depend on the current state (not the history)
- Policies are stationary (time-independent)


## References
- [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/bookdraft2018jan1.pdf) - Chapter 3: Finite Markov Decision Processes
- David Silver's RL Course Lecture 2 - Markov Decision Processes ([video](https://www.youtube.com/watch?v=lfHX2hHRMVQ), [slides](http://www0.cs.ucl.ac.uk/staff/d.silver/web/Teaching_files/MDP.pdf))

