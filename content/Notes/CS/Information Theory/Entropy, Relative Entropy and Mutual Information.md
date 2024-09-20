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
