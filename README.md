# Route-Optimization-in-Grid-World
A route optimization program using Value Iteration.
## Introduction
Imaging that we are in the grid world (Blue), there are several blocks (Black) & traps (Red) in this maze, and our goal is to arrive the destination (Green) as fast as we can. Meanwhile, we might want to avoid the traps, as a small mistake would be fatal. 

![1 1](https://user-images.githubusercontent.com/112973740/220482612-1dc26b34-0d94-4b0b-acdb-e3f20a88e426.png)
![1 4](https://user-images.githubusercontent.com/112973740/220482627-f033086d-cee5-49aa-9331-64720bb750f2.png)
![1 7](https://user-images.githubusercontent.com/112973740/220482638-c92679ba-9cac-45d4-a29a-676622f54692.png)


We could, of course, find a better way to escape. However, if the maze is large enough, it is relatively hard to optimize the route we have planed. In this case, we can apply value/policy iteration from Reinforcement Learning, to create an agent that take actions for us.

## Value Iteration vs. Policy Iteration
Value Iteration and Policy Iteration are both based on Markov Decision Process. While Value Iteration are updating Value of states, Policy Iteration tries to update Policy at each iteration.

Value iteration is designed to search for the optimized policy, as the policy could converge faster than the convergence of value. 
Here is a detailed introduction about Value Iteration and Policy Iteration from The University of Melbourne. https://gibberblot.github.io/rl-notes/single-agent/value-iteration.html [2]

Value Iteration is generally easier for coding, thus, we would use Value Iteration to optimize the route with Epsilon Greedy.

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
### Episode 1（Proper Greedy）
![1 1](https://user-images.githubusercontent.com/112973740/220482672-93fe9fc5-8c64-4c15-9627-aaac76294cad.png)
![1 2](https://user-images.githubusercontent.com/112973740/220482673-8af21547-0f4d-40a1-9d8d-5d3779b09350.png)
![1 3](https://user-images.githubusercontent.com/112973740/220482674-16af7fa2-da4b-4d3c-a157-d8a4e37d9aec.png)
 (set 1.1)

![1 4](https://user-images.githubusercontent.com/112973740/220482675-334a27d4-daa5-46a5-9a5f-e163ab0660a0.png)
![1 5](https://user-images.githubusercontent.com/112973740/220482676-5e84c2a1-7ff1-4810-a509-7be3121dd407.png)
![1 6](https://user-images.githubusercontent.com/112973740/220482677-cdb1d93b-95ac-4d5e-9baf-b4e70fec2678.png)
 (set 1.2)
 
![1 7](https://user-images.githubusercontent.com/112973740/220482678-a4b8e3fb-6862-4a9b-bf01-434f399ce41c.png)
![1 8](https://user-images.githubusercontent.com/112973740/220482680-276fce8b-7744-4e4e-ae2d-b16e605ab7b5.png)
![1 9](https://user-images.githubusercontent.com/112973740/220482681-bd2e85a4-bbc0-45b2-8169-04b1627ed81f.png)
 (set 1.3)

### Episode 2 (Always Greedy)
![2 1](https://user-images.githubusercontent.com/112973740/220483491-58637cce-4246-418a-999c-b33af1a75fbe.png)
![2 2](https://user-images.githubusercontent.com/112973740/220483492-ffff9b2e-00c3-4ee8-9586-e1462319829b.png)
![2 3](https://user-images.githubusercontent.com/112973740/220483493-67f38a02-c459-4a4b-8781-47aae66dd2bc.png)
 (set 2.1)

![2 4](https://user-images.githubusercontent.com/112973740/220483494-539edbb7-f500-4d66-a1a8-cf70599b748a.png)
![2 5](https://user-images.githubusercontent.com/112973740/220483495-f5a6106e-69c4-4a0e-88ac-950945181bb3.png)
![2 6](https://user-images.githubusercontent.com/112973740/220483497-445388b1-f796-4ea3-9f04-528258b71411.png)
 (set 2.2)

![2 7](https://user-images.githubusercontent.com/112973740/220483498-a7a4dc8d-ddd7-4b3d-8207-fc5ca41a91fa.png)
![2 8](https://user-images.githubusercontent.com/112973740/220483499-dff13b11-2d8f-495c-b54b-483be9a3429b.png)
![2 9](https://user-images.githubusercontent.com/112973740/220483500-5accf958-ccf6-44b6-9ed0-b2163ece5d7d.png)
 (set 2.3)

### Episode 3 (High Action Cost)


The policy of action is similar to the gradient descent, where the agent would always choose the direction that has the highest value of state (or take the action that has highest value of action).
## Conclusion
The optimization process is controlled by Epsilon Greedy. As shown in Episode 1, if we allow the agent to explore the system with a proper Epsilon, it would try to balance the cost and the safty by avoiding the traps. However, if we always pick the Greedy action, it would always follow the fastest route, then consider the probibility of making mistakes.

## Reference
[1] Sutton, R.S, Barto, A.G (2020) Reinforcement Learning: An Introduction

[2] Tim Miller (2022) Introduction to Reinforcement Learning
