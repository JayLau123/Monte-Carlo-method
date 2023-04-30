# Monte-Carlo-method
A brief introduction to MC method and its mathematical theory

## A statistical sampling theory to solve physical or mathematical problems approximately.

MC can be used to solve any problem having a probabilistic interpretation. By the law of large numbers, integrals described by the expected value of some random variable can be approximated by taking sample mean of independent samples of the variable. Firstly, establish a probabilistic model or probabilistic process that is associated with the problem and find the relation between the certain eigenvalues or quantities of the probability model and the solution of the problem. Next, use computer to generate some samples randomly, use these sample to estimate some eigenvalue of the distributation so as to find the numerical solution to the problem. 

#### Some problems are dealt with MC

optimization, numerical integration, deterministic mathematical problems, and probabilistic problems(diffusion of neutrons).


#### The application of MC in experimental particle physics

The probability of some physical process such as proton decay is very small, and the detection efficiency is low while the experiment cost is very high.
As a result, we may use other method to simulate the process and find a reliable numerical solution.

![1](https://user-images.githubusercontent.com/98719524/218607165-b15ad551-11cc-4acb-bd28-fdc3e792e84d.png)


The real system is the nature, we can perform any measurements to get the results. But considering the measurements sometimes are very difficult and inefficient, we can establish an approximate model with numerical method and baisc theories, then leaverage on computing techniques and cloud computational resources to solve the question. 


## Error analysis in MC

In practice, many random variables $Y$ are consisted of other random subvariables $X_k$, each single random subvariable plays a insignificant role in the total influence. Such random variable $Y$ has normal distribution approximately. Here, we use the most popular iid CLT.

The error of MC is defined as:

$$\epsilon= \dfrac{\sigma \times \lambda}{\sqrt{N}}$$

we can reduce the error by increasing the number of samples $N$, and more efficiently, choose some variable that has smaller variance $\sigma$. Besides, we can also use the convergence and confidence interval to estimate how many experiment times or how many sample we need to achieve a certain accuracy.


#### Please find more details in Error analysis in MC.ipynb


### Buffon's needle problem

<img width="400" alt="Buffon's needle problem" src="https://user-images.githubusercontent.com/98719524/218281819-26e74e6c-05dd-4949-b39a-654f6a735a27.png">

### numerical integration 

A method used in numerical analysis to calculate the definite integral of a function. It involves approximating the area under the curve of a function by dividing it into small subintervals and using numerical techniques to compute the approximate value of the integral. There are various numerical integration techniques like rectangular rule, trapezoidal rule, Simpson’s rule, Monte Carlo integratio



### Monte Carlo Tree Search (MCTS)

https://www.baeldung.com/java-monte-carlo-tree-search

A search algorithm used in decision-making tasks, particularly in games such as chess, Go, and poker. It is a heuristic algorithm that builds a search tree by traversing the tree repeatedly and selecting promising nodes that have not been explored before. The algorithm uses Monte Carlo simulations to estimate the value of each selected node and updates the estimated values of other nodes in the tree based on the simulation results.

For example, we can use a game tree to represent a game. Each node of the game tree represents a state, and the set of the next state constitutes the next node of the state. For example, any chessboard situation is a state, and all possible moves under the state are formed the next states. The collection of new situations constitutes the next nodes of the state. If it is a simple game, the optimal solution can be obtained according to the exhaustive results. But for complex games, such as Go, the number of states is more than the total number of atoms in the observable universe, and no computer can do such an exhaustive enumeration.

According to the **theorem of large numbers**, when the number of samples is large enough, the sampled samples are infinitely approximate to the **original distribution** (all situations in the real world are considered). MCTS uses random sampling as an approximate estimation method. Find the most likely node to go through a large number of self-games.(自博弈)

Self-game is a method in which the computer simulates two players (Similar to GAN), starting from the current position with a random or simple strategy. But first we need to define a strategy to select the most likely node to go in the current situation. Continuing to the secondary node and finally record the result of the self-game and update the data. Repeat this process until the stopping condition is met.

The stop condition can be after 1 hour, after 1 million self-games, if the number of self-games is infinite, the optimal solution can be found theoretically.

How to define the selection strategy? 

Upper Confidence Bound applied to Trees (UCT) is an extension of the original MCTS algorithm that has been widely used in game AI. UCT selects a node to expand based on a combination of the exploitation of the known results so far and the exploration of the unknown options. This balance between exploration and exploitation is achieved by using a UCB1 formula.

$$UCT=\dfrac{Q_i}{N_i}+C\sqrt{\dfrac{ln(T)}{N_i}}$$

The first term is winning percentage $WP=\dfrac{Q_i}{N_i}$

where $Q_i$ is the number of times $i$th node wins, $N_i$ is the number of visits to the $i$th node, $C$ is a constant used to adjust the weight of the game times, and $T$ is the total number of visits. 

As the number of visits increases, the value of the second item becomes increasingly smaller. $UCT$ tends to choose those nodes that have not been visited many times to avoid the problem of high winning percentage and low confidence rate. The self-game process is repeated continuously, and each time the node with the highest value of $UCT$ is selected. After repeating many times, the node with the highest number of visits is the best node.

## Random number

In practical applications, randomness is an essential and basic demand for almost all MC. It is also used in network security to encrypt data and communication, and to perform simulation analysis in many fields. The simplest understanding, such as game lottery, requires good randomness to ensure its fairness. We may use quantum computer to generate quantum random number.







