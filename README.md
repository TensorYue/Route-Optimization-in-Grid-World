# Route-Optimization-in-Grid-World
A route optimization program using Value Iteration.
## Introduction
Imaging that we are in the grid world (Blue), there are several blocks (Black) & traps (Red) in this maze, and your goal is to arrive the destination (Green) as fast as we can. Meanwhile, we might want to avoid the traps, as a small mistake would be fatal. 

![Map1](https://user-images.githubusercontent.com/112973740/220216808-8cf8483f-72d5-426a-9431-74ef1f9db24a.png)

We could, of course, find a better way to escape. However, if the maze is large enough, it is relatively hard to optimize the route you have planed. In this case, we can apply value/policy iteration from Reinforcement Learning, to create an agent that take actions for us.

## Value Iteration vs. Policy Iteration
Value iteration is designed to search for the optimized policy, as the policy could converge faster than the convergence of value. (Here is an example for showing these difference https://gibberblot.github.io/rl-notes/single-agent/value-iteration.html)

## Result with Value Iteration
![Map1](https://user-images.githubusercontent.com/112973740/220216824-35b297f4-189c-4718-8b36-f92079f3713d.png)
![Value1](https://user-images.githubusercontent.com/112973740/220216830-1a0792cf-48c5-4c40-be5a-99ba57fb7bde.png)
![Route1](https://user-images.githubusercontent.com/112973740/220216860-cbf85462-4641-45bd-987e-f5e8fca1de34.png)
![Map2](https://user-images.githubusercontent.com/112973740/220217251-01466b41-8a80-498d-ac3d-53ef18bc2370.png)
![Value2](https://user-images.githubusercontent.com/112973740/220217260-067cabe1-72ef-4b17-b7f1-9bf529c67ea5.png)
![Route2](https://user-images.githubusercontent.com/112973740/220217257-ee5fa6c0-efad-48b0-9976-e784bd60a460.png)
![Map3](https://user-images.githubusercontent.com/112973740/220217488-747e8c6d-500c-4032-a1c9-b1f31e0f642d.png)
![Value3](https://user-images.githubusercontent.com/112973740/220217498-739f5528-87f3-4355-a95e-a89e4f8b4b02.png)
![Route3](https://user-images.githubusercontent.com/112973740/220217511-73349d3c-4827-4155-918c-7eee5a99c558.png)

The policy of action is similar to the gradient descent, where the agent would always choose the direction that has the highest value of state (or take the action that has highest value of action).
## Conclusion
When we are dealing with a larger system, we may need to have a larger discountnig factor as well as a smaller reward, because the propogation of value might dissipate over time.

## Reference
Sutton, R.S, Barto, A.G (2020) Reinforcement Learning: An Introduction

Tim Miller (2022) Introduction to Reinforcement Learning
