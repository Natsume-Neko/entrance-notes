## Pushdown Automata(PDA)
### Definition
A pushdown automata involves seven components:
$$
P = (Q, \Sigma, \Gamma, \delta, q_0, Z_0, F)
$$
- A finite set of states $Q$
- A finite set of input symbols $\Sigma$
- A finite stack alphabet $\Gamma$
- The transition funtion $\delta$. It takes a triple as arguments $\delta(q, a, X)$, $q \in Q, a \in \Sigma, X \in \Gamma$. And it outputs a pair $(p, \gamma)$, $p$ is the new state and $\gamma$ is the string of stack symbols that replaces $X$. 
- The start state $q_0$
- The start stack symbol $Z_0$
- The set of final states $F$
## The Language of PDA
- Acceptance by final state and acceptance by empty stack(equivalent)
- Equivalence of PDA's and CFG's
