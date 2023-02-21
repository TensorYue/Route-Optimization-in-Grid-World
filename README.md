# Route-Optimization-in-Grid-World
A route optimization program using Value Iteration.
## Introduction
Imaging that we are in the grid world, there are several blocks & traps in this maze, and your goal is to arrive the destination as fast as we can. Meanwhile, we might want to avoid the traps, as a small mistake would be fatal. 

![Map1](https://user-images.githubusercontent.com/112973740/220216808-8cf8483f-72d5-426a-9431-74ef1f9db24a.png)

We could, of course, find a better way to escape. However, if the maze is large enough, it is relatively hard to optimize the route you have planed. In this case, we can apply value/policy iteration from Reinforcement Learning, to create an agent that take actions for us.

## Value Iteration vs. Policy Iteration
Value iteration is designed to search for the optimized policy, as the policy could converge faster than the convergence of value. (Here is an example for showing these difference https://gibberblot.github.io/rl-notes/single-agent/value-iteration.html)

## Agent with Value Iteration
![Map1](https://user-images.githubusercontent.com/112973740/220216824-35b297f4-189c-4718-8b36-f92079f3713d.png)
![Value1](https://user-images.githubusercontent.com/112973740/220216830-1a0792cf-48c5-4c40-be5a-99ba57fb7bde.png)
![Route1](https://user-images.githubusercontent.com/112973740/220216860-cbf85462-4641-45bd-987e-f5e8fca1de34.png)

The policy of action is similar to the gradient descent, where the agent would always choose the direction that has the highest value of state (or take the action that has highest value of action).
## Conclusion
When we are dealing with a larger system, we may need to have a larger discountnig factor as well as a smaller reward, because the propogation of value might dissipate over time.

## Reference
Sutton, R.S, Barto, A.G (2020) Reinforcement Learning: An Introduction

Tim Miller (2022) Introduction to Reinforcement Learning
