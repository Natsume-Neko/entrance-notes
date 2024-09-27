## Entropy
### Definition
Entropy $H(X)$ of a discrete random variable $X$:
$$
H(X) = -\Sigma _{x \in X}\ p(x)log\ p(x)
$$
Expected value form:
$$
H(X) = E_p log\ {\frac{1}{p(X)}}
$$
## Joint Entropy and Conditional Entropy
### Joint Entropy
#### Definition
$$
H(x, y) = -\Sigma _{x \in X} \Sigma _{y \in Y} \ p(x,y)log\ p(x, y)
$$
Expected value form:
$$
H(x, y) = -E\ log\ p(X, Y)
$$
### Conditional Entropy
#### Definition
$$
H(Y | X) = -\Sigma _{x \in X}\Sigma _{y \in Y}\ p(x, y) log\ p(y | x)
$$
Expected value form:
$$
H(Y | X) = -E\ log\ p(Y | X)
$$
#### Chain Rule
$$
H(X, Y) = H(X) + H(Y | X)
$$
## Relative Entropy and Mutual Information
### Relative Entropy
#### Definition
Relative entropy is a measure of the distance between two variables.
The relative entropy or Kullback–Leibler distance between two probability mass functions $p(x)$ and $q(x)$ is defined as
$$
\begin{aligned}
D(p||q) &= \Sigma _{x\in X}\ p(x)log\ \frac{p(x)}{q(x)} \\ &=E_p\ log\ \frac{p(X)}{q(X)}
\end{aligned}
$$
### Mutual Information
#### Definition
It is the reduction in the uncertainty of one random variable due to the knowledge of the other.
$$
\begin{aligned}
I(X;Y) &= \Sigma _{x\in X}\Sigma _{y\in Y}\ p(x, y)log\ \frac{p(x,y)}{p(x)p(y)} \\
&= D(p(x,y)||p(x)p(y)) \\ 
&= E_{p(x,y)}log\ \frac{p(X,Y)}{p(X)p(Y)}
\end{aligned}
$$
#### Relationship Between Entropy
$$
\begin{aligned}
I(X;Y) &=\Sigma _{x\in X}\Sigma _{y\in Y}\ p(x,y)log\ \frac{p(x|y)}{p(x)}\\
&= H(X)-H(X|Y) \\ 
&= H(Y) - H(Y|X) \\ 
&= H(X) + H(Y) - H(X, Y)
\end{aligned}
$$
## Chain Rules
### Chain Rule for Entropy
$$
H(X_1, X_2,\ ..., X_n) = \Sigma _{i=1}^{n}H(X_i|\ X_{i-1},...,X_1)
$$
### Chain Rule for Information
#### Conditional Mutual Information
$$
\begin{aligned}
I(X;Y|Z) &= H(X|Z) - H(X|Y,Z)\\
&= E_{p(x,y,z)} log\ \frac{p(X,Y|Z)}{p(X|Z)p(Y|Z)}
\end{aligned}
$$
#### Chain Rule for Information
$$
I(X_1,X_2,...,X_n;Y) = \Sigma _{i=1}^{n}I(X_i;Y|X_1,X_2,...,X_{i-1})
$$
### Chain Rule for Relative Entropy
#### Conditional Relative Entropy
$$
\begin{aligned}
D(p(y|x)||q(y|x)) &= \Sigma _{x}p(x) \Sigma _{y}p(y|x)\ log\ \frac{p(y|x)}{q(y|x)} \\
&= E_{p(x,y)}log \frac{p(Y|X)}{q(Y|X)}
\end{aligned}
$$
#### Chain Rule for Relative Entropy
$$
D(p(x,y)||q(x,y)) = D(p(x)||q(x)) + D(p(y|x)||q(y|x))
$$
## Jensen's Inequality
### Jensen's Inequality
When $f(x)$ is a convex funtion:
$$
E(f(x)) \ge f(E(x))
$$
We can prove this using induction.
### Applications
#### Information Inequality
$$
D(p||q) \ge 0
$$
## Log Sum Inequality
### Log Sum Inequality
$$
\Sigma _{i=1}^{n} a_i log\ \frac{a_i}{b_i} \ge (\Sigma _{i=1}^{n} a_i) log\ \frac{\Sigma _{i=1}^{n}a_i}{\Sigma _{i=1}^{n}{b_i}}
$$
### Applications
- Convexity of relative entropy
- Concavity of entropy
- The mutual information $I(X;Y)$ is a concave function of $p(x)$ for fixed $p(y|x)$ and a convex function of $p(y|x)$ for fixed $p(x)$.
## Data Processing Inequality
### Markov Chain
Random variables $X$, $Y$, $Z$ are said to form a Markov chain in that order (denoted by $X → Y → Z$) if the conditional distribution of $Z$ depends only on $Y$ and is conditionally independent of $X$. Specifically, $X$, $Y$, and $Z$ form a Markov chain $X → Y → Z$ if the joint probability mass function can be written as:
$$
p(x, y, z) = p(x)p(y|x)p(z|y)
$$
### Data Processing Inequality
If $X \rightarrow Y \rightarrow Z$, then $I(X;Y) \ge I(X;Z)$.
## Fano's Inequality
For any estimator $\hat{X}$ such that $X → Y → \hat{X}$, with $P_e = Pr(X \ne \hat{X})$, we have:
$$
H(P_e)+P_elog|X| \ge H(X|\hat{X}) \ge H(X|Y)
$$
