## Channel Model
### Discrete channel
We define a discrete channel to be a system consisting of an input alphabet $\mathcal{X}$ and output alphabet $\mathcal{Y}$ and a probability transition matrix $p(y|x)$ that expresses the probability of observing the output symbol $y$ given that we send the symbol $x$.

### Channel Capacity
We define the “information” channel capacity of a discrete memoryless channel as
$$
C = \underset{p(x)}{max}I(X;Y)
$$
## Symmetric Channels
A channel is said to be symmetric if the rows of the channel transition matrix $p(y|x)$ are permutations of each other and the columns are permutations of each other. 
A channel is said to be weakly symmetric if every row of the transition matrix $p(-|x)$ is a permutation of every other row and all the column sums $\Sigma _x p(y|x)$ are equal.
For a weakly symmetric channel:
$$
C = log|\mathcal{Y}| + H(row\ of\ transition\ matrix)
$$
## Examples
- Binary Symmetric Channel (BSC)
- Binary Erasure Channel
- 2元対称消失通信路
- 2元対称通信路の直列接続
- 加法的2元通信路
- 2元対称通信路の並列接続
## Channel Coding
### Code Rate
#### Code Rate
$$
R = \frac{log_2M}{n}
$$
$$
R_{max} = log_2\ r
$$
#### Efficiency of Code Rate (符号化率)
$$
\eta = \frac{R}{R_{max}}
$$
#### Redundancy
$$
\rho = 1 - \eta
$$
## Maximum Likelihood Decoding
Suppose:
$$
P_c(w_i) = \Sigma _{y \in \Omega _i} P(y|w_i)
$$
The maximum likelihood decoding maximizes:
$$
P_c = \frac{1}{M} \Sigma _{i=1}^{M}P_c (w_i)
$$
- Random Coding
- Channel Coding Theorem
- ...
## Channel Coding Methods
### Definitions
- Linear Code: check bit $c$ is a linear function of information bits (data bits).
### Parity Check Code
- Single Parity Check
- Horizontal Vertical Parity Check
### Hamming Code
#### Definitions
- Generator Matrix
- Parity Check Matrix
#### Composition Rules
- Code Length: $n = 2^m - 1$
- Information Length: $k = 2^m - 1 - m$
- Check Bits: $m$
### Cyclic Code
#### Definitions
- Generator polynomial
- Cycle/Period of a generator polynomial
#### Composition Rules
- Use $G(x) | (x^n - 1)$ as generator function (primitive polynomial)
- Information Bits: $X(x)$
- $X(x)x^m = A(x)G(x) + C(x)$
- $W(x) = X(x)x^m + C(x)$
- Code Length: $n = 2^m - 1$
- Information Length: $k = 2^m - 1 - m$
- Check Bits: $m$
#### Circuits
- Decoder 符号器
- Divider 除算器