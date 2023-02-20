# Route-Optimization-in-Grid-World
A route optimization program using Value Iteration.
## Introduction
Imaging that we are in the grid world, there are several blocks & traps in this maze, and your goal is to arrive the destination as fast as we can. Meanwhile, we might want to avoid the traps, as a small mistake would be fatal. 

![grid_world](https://user-images.githubusercontent.com/112973740/220184904-85efffdc-4c38-499e-9ece-6ca8357cb013.png)

We could, of course, find a better way to escape. However, if the maze is large enough, it is relatively hard to optimize the route you have planed. In this case, we can apply value/policy iteration from Reinforcement Learning, to create an agent that take actions for us.

## Value Iteration vs. Policy Iteration
Value iteration is designed to search for the optimized policy, as the policy could converge faster than the convergence of value. (Here is an example for showing these difference https://gibberblot.github.io/rl-notes/single-agent/value-iteration.html)

## Agent with Value Iteration
![Maze](https://user-images.githubusercontent.com/112973740/220182999-a15729a7-ce56-4c29-8aae-80b11b98fcb1.png)
![solution](https://user-images.githubusercontent.com/112973740/220183956-bd6939f8-7974-4c4a-9936-5926c81a1b8c.png)

The policy of action is similar to the gradient descent, where the agent would always choose the direction that has the highest value of state (or take the action that has highest value of action).
## Conclusion
When we are dealing with a larger system, we may need to have a larger discountnig factor as well as a smaller reward, because the propogation of value might dissipate over time.

## Reference
Sutton, R.S, Barto, A.G (2020) Reinforcement Learning: An Introduction

Tim Miller (2022) Introduction to Reinforcement Learning
