Combinator: A function without free variables
Calculus: A method of computation or calculation in a special notation

# SKI Calculus
Indentity Function:
$$
I\ x \to x
$$
Constant Function:
$$
K\ x\ y \to x
$$
Generalized Function Application:
$$
S\ x\ y\ z \to (xz)\ (yz)
$$
## Definition
- Terms
- Terms are trees: $S\ x\ y\ z\ =\ (((S\ x)\ y)\ z)$

## Rewrite Rules
- Rewrite: $\to$
- Reflexive, transitive closure of Rewrite: $\to^*$ (Rewrite zero or more times)

## Programming
### General Recursion
- $(S\ I\ I)\ (S\ I\ I)$: Non-terminating expression
- $x\ =\ S\ (K\ f)\ (S\ I\ I)$
- $SIIx \to^* xx \to^* f(xx) \to^* f(f(xx))$
### Booleans
- $Txy \to x$
- $Fxy \to y$
- $T = K$
- $F = SK$
- ...
### Systematic approach to write combinators
Using abstract algorithm first, replace them with SKI to eliminate.
- $A(X, X) = I$
- $A(E, X) = KE$
- $A(E1\ E2, X) = SA(E1, X)A(E2, X)$
- Improvement...


