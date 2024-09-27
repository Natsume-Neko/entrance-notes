## Deterministic Finite Automata(DFA)
### Definition
A deterministic finite automata consists of:
- A finite set of states $Q$.
- A finite set of input symbols $\Sigma$.
- A transition function $\delta$ which takes a state $q$ from $Q$ and an input symbol $a$ from $\Sigma$ as inputs, and outputs a state $p$ from $Q$  ($\delta(q, a) = p$).
- A start state $q_0$, which is one of the states in $Q$.
- A set of final or accept state $F$, which is a subset of $Q$.
Thus a DFA can be denote as a five-tuple:
$$
A = (Q, \Sigma , \delta , q_0, F)
$$

