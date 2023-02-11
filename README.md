# Monte-Carlo-method
A brief introduction to MC method and its mathematical theory

### A statistical sampling theory to solve physical or mathematical problems approximately.

MC can be used to solve any problem having a probabilistic interpretation. By the law of large numbers, integrals described by the expected value of some random variable can be approximated by taking sample mean of independent samples of the variable. Firstly, establish a probabilistic model or probabilistic process that is associated with the problem and find the relation between the certain eigenvalues or quantities of the probability model and the solution of the problem. Next, use computer to generate some samples randomly, use these sample to estimate some eigenvalue of the distributation so as to approximate the solution to the problem. 

### Some problems are dealt with MC

optimization, numerical integration, deterministic mathematical problems, and probabilistic problems(diffusion of neutrons).


### Error analysis in MC

Let's start from Central Limit Theorem (CLT). 

In practice, many random variables $Y$ are consisted of other random subvariables $X_k$, each single random subvariable plays a insignificant role in the total influence. Such random variable $Y$ has normal distribution approximately.

Here, we use the most popular iid CLT.

For independent identical distributed(iid) random variables $X_1, X_2, X_3...$, and they share the same expactation and variance: $E(X_k)=\mu, D(X_k)=\sigma^2, (k=1,2,3...)$, so the summation of these iid random variables is:

$$\sum_{k=1}^{n}X_k$$

so the standardized variable is:

$$Y_n=\dfrac{\sum_{k=1}^n X_k-E\left(\sum_{k=1}^n X_k\right)}{\sqrt{D\left(\sum_{k=1}^n X_k\right)}}=\dfrac{\sum_{k=1}^n X_k-n \mu}{\sqrt{n} \sigma}$$


#### (Note: we can convert any normal distribution $N(\mu, \sigma^2)$ into standard normal distribution N(0,1))

For any value of x, the distributation $F_n(x)$ has:

$$\lim _{n \rightarrow \infty} F_n(x) =\lim _{n \rightarrow \infty} P\left\{\frac{\sum_{k=1}^n X_k-n \mu}{\sqrt{n} \sigma} \leqslant x\right\} =\int_{-\infty}^x \frac{1}{\sqrt{2 \pi}} \mathrm{e}^{-t^2 / 2} \mathrm{~d} t=\Phi(x)$$

Therfore, when $n$ is large enough:

$$\dfrac{\sum_{k=1}^n X_k-n \mu}{\sqrt{n} \sigma} \sim N(0,1) $$

For explicit interpretation, we can rewrite the formual above in this way:

$$\dfrac{\dfrac{1}{n} \sum_{k=1}^n X_k-\mu}{(\sigma / \sqrt{n})}=\dfrac{\overline{X}-\mu}{(\sigma / \sqrt{n})}$$

The meaning of the new form is that independent identically distributed(iid) random variables $X_1, X_2, X_3...$ that share the same expactation and variance: $E(X_k)=\mu, D(X_k)=\sigma^2, (k=1,2,3...)$, their arithmetic average: $\overline{X}=\dfrac{1}{n} \sum_{k=1}^n X_k$ has the normal distribution with mean is $\mu$ and variance is $\dfrac{\sigma^2}{n}$, when $n$ is large enough. 

Actually, this is the basic theory of Large sample statistics.


, tends towards the standard normal distribution when the number of random variables is big enough, even if the original variables themselves are not normally distributed.



The error of MC is defined as:

$$\epsilon= \dfrac{\sigma \times \lambda}{\sqrt{N}}$$

$\lambda$ is related to the condidence level $1-\alpha$ 









### Buffon's needle problem

<img width="400" alt="Buffon's needle problem" src="https://user-images.githubusercontent.com/98719524/218281819-26e74e6c-05dd-4949-b39a-654f6a735a27.png">











