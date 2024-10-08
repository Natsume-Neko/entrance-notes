## Pumping Lemma
Let $L$ be a regular language. Then there exists a constant $n$(which depends on $L$) such that for every string $w$ in $L$  such that $|w| \ge n$, we can break $w$ into three strings, $w = xyz$, such that:
1. $y \ne \varepsilon$
2. $|xy| \le n$
3. For all $k \ge 0$, the string $xy^kz$ is also in $L$
### Application
- Prove a language is not a regular language
## Minimization of DFA
- Table filling algorithm
