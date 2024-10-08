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
### Describe DFA
- Transition Diagram
- Transition Table
### The Language of DFA
$$
L(A) = \{ w|\ \hat{\delta}(q_0, w) \in F  \}
$$
## Nondeterministic Finite Automata(NFA)
### Definition
- Essentially same as DFA.
- The difference is in $\delta$ : $\delta$ in NFA returns a set of states while in DFA is a single state.
### The Language of NFA
$$
L(A) = \{ w|\ \hat{\delta}(q_0, w) \cap F \ne \emptyset \}
$$
### Equivalence of DFA and NFA
#### Proof
1. Subset construction
2. Induction
## NFA with $\varepsilon$-Transitions
### Definition
- Essentially same as NFA
- Except that the input of $\delta$ is $Q$ and $\Sigma \cup \{\varepsilon\}$
### Epsilon Closures
$$
ECLOSE(S)
$$
### Eliminating $\varepsilon$ transitions
The equivalence between $\varepsilon$-NFA and DFA.
Also use subset construction to prove.
