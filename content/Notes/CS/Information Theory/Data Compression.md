## Codes
### Expect Length
$$
L(C) = \Sigma _{x \in \mathcal{X}}\ p(x)l(x)
$$
### Nonsingular
A code is said to be nonsingular if every element of the range of $X$ maps into a different string in $D^∗$.
### Extension
The extension $C^∗$ of a code $C$ is the mapping from finite-length strings of $X$ to finite-length strings of $D$.
### Uniquely Decodable
A code is called uniquely decodable if its extension is nonsingular.
### Prefix Code
A code is called a prefix code or an instantaneous code if no codeword is a prefix of any other codeword.
## Kraft Inequality
For any instantaneous code (prefix code) over an alphabet of size $D$, the codeword lengths $l_1, l_2, . . . , l_m$ must satisfy the inequality:
$$
\Sigma _i D^{-l_i} \le 1
$$
Conversely, given a set of codeword lengths that satisfy this inequality, there exists an instantaneous code with these word lengths.
### McMillan
The above inequality holds for any uniquely decodable $D$-ary code.
## Optimial codes
The expected length $L$ of any instantaneous $D$-ary code for a random variable $X$ is greater than or equal to the entropy $H_D (X)$:
$$
L \ge H_D(X)
$$
## Huffman Codes
### Procedure
It builds a $D$-ary tree. Each time it chooses $D$ least frequent symbols and merges them to form an inner node, until there's only one node(root).
### Optimality
It can be proved that the Huffman Code is optimal. That is, no other code can get a less expected length less than Huffman Code.
## Block Code
### Extended Information Source
When combining $n$ symbols from orignial alphabet, we can create a new extended information source, which is called $n$-th order extended information source, write as $S^n$
### Bounds
$$
H(S^n) \le L_n < H(S^n) + 1
$$
### n-th Order Entropy
$$
H_n(S) = \frac{H(S^n)}{n}
$$
### Entropy (Rate)
$$
H(S) = lim_{n \to \infty} H_n(S)
$$
#### Entropy Rate of Markov Chain
$$
H(S) = \Sigma _i \mu _i (-\Sigma _j P_{ij}log\ P_{ij})
$$
## Arithmetic Coding
- Incremental
- Could be used for any block length
## Run Length Coding
