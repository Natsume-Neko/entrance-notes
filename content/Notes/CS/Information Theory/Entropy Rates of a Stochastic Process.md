## Stochastic process
A stochastic process $\{X_i\}$ is an indexed sequence of random variables. In general, there can be an arbitrary dependence among the random variables.
### Stationary Stochastic Process
A stochastic process is said to be stationary if the joint distribution of any subset of the sequence of random variables is invariant with respect to shifts in the time index:
$$
\begin{aligned}
Pr(X_1=x_1, X_2=x_2, ...,X_n=x_n) \\
= Pr(X_{1+l}=x_1, X_{2+l}=x_2, ..., X_{n+l}=x_n)
\end{aligned}
$$
## Markov Chain
A discrete stochastic process $X_1, X_2, . . .$ is said to be a Markov chain or a Markov process if:
$$
\begin{aligned}
Pr(X_{n+1}=x_{n+1}|X_n=x_n,X_{n-1}=x_{n-1},...,X_1=x_1) \\
=Pr(X_{n+1}=x_{n+1}|X_n=x_n)
\end{aligned}
$$

### Time Invariant
The Markov chain is said to be time invariant if the conditional probability $p(x_{n+1}|x_n)$ does not depend on $n$. We will assume that the Markov chain is time invariant unless otherwise stated.
#### Transition Matrix
A time-invariant Markov chain is characterized by its initial state and a probability
transition matrix $P = [P_{ij}], i, j \in \{1, 2, . . . , m\}$, where $P_{ij} = Pr(X_{n+1} =j|X_n = i)$.
If the probability mass function of the random variable at time $n$ is $p(x_n)$, the probability mass function at time $n + 1$ is:
$$
p(x_{n+1})=\Sigma _{x_n} p(x_n)P_{x_nx_{n+1}}
$$
## Entropy Rate
The entropy of a stochastic process $\{X_i\}$ is defined by:
$$
H(\mathcal{X}) = lim_{n\to \infty}\frac{1}{n}H(X_1,X_2,...,X_n)
$$
A related quantity for entropy rate:
$$
H'(\mathcal{X})=lim_{n\to \infty}H(X_n|X_1,X_2,...,X_{n-1})
$$
For a stationary stochastic process, the above 2 limits exists and:
$$
H(\mathcal{X}) = H'(\mathcal{X})
$$
To prove, use $Ces\acute{a}ro\ mean$.
### Markov Chain
For a stationary Markov chain, the entropy rate is:
$$
H(\mathcal{X})=H'(\mathcal{X})=lim_{n\to \infty}H(X_n|X_1,X_2,...,X_{n-1})
=lim_{n\to \infty}H(X_n|X_{n-1})=H(X_2|X_1)
$$
To calculate the stationary distribution, solve the following equation:
$$
\begin{aligned}
&\Sigma _i \mu _i = 1 \\
&\mu _i = \Sigma _j \mu _j p_{ji}
\end{aligned}
$$


