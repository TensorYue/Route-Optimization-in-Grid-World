# Route-Optimization-in-Grid-World
A route optimization program using Value Iteration.
## Introduction
Imaging that we are in the grid world (Blue), there are several blocks (Black) & traps (Red) in this maze, and your goal is to arrive the destination (Green) as fast as we can. Meanwhile, we might want to avoid the traps, as a small mistake would be fatal. 

![Map1](https://user-images.githubusercontent.com/112973740/220216808-8cf8483f-72d5-426a-9431-74ef1f9db24a.png)

We could, of course, find a better way to escape. However, if the maze is large enough, it is relatively hard to optimize the route you have planed. In this case, we can apply value/policy iteration from Reinforcement Learning, to create an agent that take actions for us.

## Value Iteration vs. Policy Iteration
Value Iteration and Policy Iteration are both based on Markov Decision Process. While Value Iteration are updating Value of states, Policy Iteration tries to update Policy at each iteration.

Value iteration is designed to search for the optimized policy, as the policy could converge faster than the convergence of value. 
Here is a detailed introduction about Value Iteration and Policy Iteration from The University of Melbourne. https://gibberblot.github.io/rl-notes/single-agent/value-iteration.html [2]

Value Iteration is generally easier for coding, thus, we would use Value Iteration to optimize the route.

## Code Instruction & List
### Instruction
To run the code, set up the parameter and run Generate_Map, Value_Iteration, Route_Optimization in sequence.
### List
function Generate_Map

function generate_start

function generate_finish

function show_RGB

function Value_Iteration

function Route_Optimization

## Result with Value Iteration
Grid Map, Value Map, Route Map
### Episode 1（Fully connected）
![Map1](https://user-images.githubusercontent.com/112973740/220216824-35b297f4-189c-4718-8b36-f92079f3713d.png)
![Value1](https://user-images.githubusercontent.com/112973740/220216830-1a0792cf-48c5-4c40-be5a-99ba57fb7bde.png)
![Route1](https://user-images.githubusercontent.com/112973740/220216860-cbf85462-4641-45bd-987e-f5e8fca1de34.png)
![Map2](https://user-images.githubusercontent.com/112973740/220217251-01466b41-8a80-498d-ac3d-53ef18bc2370.png)
![Value2](https://user-images.githubusercontent.com/112973740/220217260-067cabe1-72ef-4b17-b7f1-9bf529c67ea5.png)
![Route2](https://user-images.githubusercontent.com/112973740/220217257-ee5fa6c0-efad-48b0-9976-e784bd60a460.png)
![Map3](https://user-images.githubusercontent.com/112973740/220217488-747e8c6d-500c-4032-a1c9-b1f31e0f642d.png)
![Value3](https://user-images.githubusercontent.com/112973740/220217498-739f5528-87f3-4355-a95e-a89e4f8b4b02.png)
![Route3](https://user-images.githubusercontent.com/112973740/220217511-73349d3c-4827-4155-918c-7eee5a99c558.png)
### Episode 2 (Partial connected)
![1Map](https://user-images.githubusercontent.com/112973740/220220536-f0411c7e-e16b-45ea-9189-da498f924a28.png)
![1Value](https://user-images.githubusercontent.com/112973740/220220551-1120fe74-576f-4007-adda-628d1f660294.png)
![1Route](https://user-images.githubusercontent.com/112973740/220220561-a9c2b82b-a60b-4d0e-8d4c-e557a168d20e.png)
![2Map](https://user-images.githubusercontent.com/112973740/220220571-2cc80223-9479-41a5-8db6-5e3833263280.png)
![2Value](https://user-images.githubusercontent.com/112973740/220220574-2a7738eb-8bbb-4867-84a5-61ec332eece4.png)
![2Route](https://user-images.githubusercontent.com/112973740/220220582-64b35967-a927-4547-b235-40af9e494f4e.png)
![3Map](https://user-images.githubusercontent.com/112973740/220220602-fbb47412-0d70-412c-9d5f-1912fa489327.png)
![3Value](https://user-images.githubusercontent.com/112973740/220220608-1002d3bc-3db9-481c-88ed-e59e408c5a39.png)
![3Route](https://user-images.githubusercontent.com/112973740/220220616-2c0a5029-ee92-4bdc-9960-03f908aa44a4.png)
### Episode 3 (Inproper discounting factor)
![a1](https://user-images.githubusercontent.com/112973740/220221583-066e1d59-95d0-4412-89d7-f348f4517bea.png)
![a2](https://user-images.githubusercontent.com/112973740/220221595-045a40f1-5197-47e3-9dd8-25b4da8a0459.png)
![a3](https://user-images.githubusercontent.com/112973740/220221600-a1929830-e45e-460e-b8fa-b4ccbc2ea8f1.png)
![b1](https://user-images.githubusercontent.com/112973740/220221614-d10776be-cb7e-48e0-afdd-707a3bd5a242.png)
![b2](https://user-images.githubusercontent.com/112973740/220221618-e4b875cb-5293-473b-9de5-0428504dcc0b.png)
![b3](https://user-images.githubusercontent.com/112973740/220221627-68438e64-03c4-42e9-8286-87d2a1433bab.png)
![c1](https://user-images.githubusercontent.com/112973740/220221637-ed61f1af-cb43-4760-a216-08ac0b0544fa.png)
![c2](https://user-images.githubusercontent.com/112973740/220221641-35e93eba-2aa9-481b-a761-ab1281029789.png)
![c3](https://user-images.githubusercontent.com/112973740/220221647-746fa6d8-8b55-483c-9733-2c213ca1fbab.png)

The policy of action is similar to the gradient descent, where the agent would always choose the direction that has the highest value of state (or take the action that has highest value of action).
## Conclusion
When we are dealing with a larger system, we may need to have a larger discountnig factor as well as a smaller reward, because the propagation of value might dissipate over time (compare Episode 1 with Episode 3).

The propagation rule is defined by Markov Decision Process. In this case, the states are only being connected with the adjacent states, and the propagation is bounded by the blocks and traps (compare Episode 1 with Episode 2).

## Reference
[1] Sutton, R.S, Barto, A.G (2020) Reinforcement Learning: An Introduction

[2] Tim Miller (2022) Introduction to Reinforcement Learning
