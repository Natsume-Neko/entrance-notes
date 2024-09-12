## Definition
A circuit is combinational if:
- Every circuit element is itself combinational
- Every node is either designated as an input or connects to exactly one output terminal
- No cyclic paths
## Boolean Equations
- Sum-of-Products Form
- Product-of-Sums Form
## Boolean Algebra
- De Morgan's Theorem
- Perfect Induction: Show the equation holds through the truth table
### Schematics
Guidelines to design the schematics
![[Pasted image 20240912134201.png]]
## Multilevel Combinational Logic
- Bubble Pushing
## X and Z
- X: illegal value(Contention)
- Z: floating value
- Tristate Buffer
## Karnaugh Maps
- Circular Thinking
- Don't cares
## Combinational Building Blocks
- Full adder
- Priority circuits
### Multiplexer
- Choose an output from serveral possible inputs based on the select signal
- Multiplexer Logic: $2^{n-1}$-inputs multiplexer could build any $n$-inputs boolean function
### Decoder
- One-hot outputs of the input
- Each output is a minterm
## Timing
- Propagation and contamination delay
- Glitches: single input transition could be solved by adding redundant terms(Karnaugh map)