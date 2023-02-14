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


The real system is the nature, we can perform any measurements to get the results. But considering the measurements sometimes are very difficult and inefficient, we can establish an approximate model with numerical method and baisc theories, then leaverage on computing techniques and cloud computational resources to solve the questions. 




## Error analysis in MC

In practice, many random variables $Y$ are consisted of other random subvariables $X_k$, each single random subvariable plays a insignificant role in the total influence. Such random variable $Y$ has normal distribution approximately. Here, we use the most popular iid CLT.

The error of MC is defined as:

$$\epsilon= \dfrac{\sigma \times \lambda}{\sqrt{N}}$$

#### Attached please find more details in Error analysis in MC.ipynb




### Buffon's needle problem

<img width="400" alt="Buffon's needle problem" src="https://user-images.githubusercontent.com/98719524/218281819-26e74e6c-05dd-4949-b39a-654f6a735a27.png">


To be continued...








