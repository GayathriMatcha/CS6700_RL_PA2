# CS6700: Reinforcement Learning 
PA2 NS24Z111 EE21S048 April 06, 2024 Assignment 2
Team Members:
* Ragu B (NS24Z111)
* Matcha Naga Gayathri (EE21S048)

---
## Dueling-DQN:
The state value function V(s) represents the value of being in a particular state regardless of the action taken, while the advantage function A(s, a) captures the additional value gained by taking a specific action ‘a’ in that state s. The Q-value Q(s, a) is then reconstructed from these two functions as
Q(s, a)=V(s)+A(s, a)−mean(A(s,⋅))
where mean(A(s,⋅)) is the mean advantage value across all actions in the state.

## INFERENCE:
Adding a baseline to REINFORCE can make it learn much faster, as shown in plot 3 and plot 4.
Variance Reduction:
The baseline helps to reduce the variance of the policy gradient estimates, leading to more stable learning.
Bias:
Adding a baseline introduces bias into the gradient estimate, but it often leads to faster convergence and improved sample efficiency.
Policy Improvement:
REINFORCE with a baseline can result in faster policy improvement compared to REINFORCE without a baseline, especially in environments with high variance in rewards.
Exploration vs. Exploitation:
The choice of baseline affects the balance between exploration and exploitation. A good baseline can help the agent focus on exploring promising regions of the state space while exploiting valuable actions.
In summary, while both REINFORCE with and without a baseline use the Monte Carlo Policy Gradient method, the inclusion of a baseline can lead to more efficient and stable learning by reducing variance and improving sample efficiency.

