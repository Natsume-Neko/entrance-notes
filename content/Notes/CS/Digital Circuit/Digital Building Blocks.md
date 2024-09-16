## Arithmatic Circuits
### Adder
#### Half Adder
- Sum $S$ and Carry out $C_{out}$
- No carry in
#### Full Adder
- Carry in $C_{in}$
#### Carry Propagate Adder(CPA)
- $N$ inputs and outputs
##### Ripple Carry Adder 
- Chain together $N$ full adders
- Slow
##### Carry Lookahead Adder
- Generate signal($G$), Propagate signal($P$)
- $G = A_i B_i$
- $P = A_i + B_i$
- Breaking into blocks
- Calculate $G_{i:j}$ and $P_{i:j}$
- $C_i = G_{i:j} + P_{i:j}C_{j}$
- Much faster
### Subtractor
- $A + B = A + \bar{B} + 1$
- Use an invertor
### Comparator
- Equality comparator: check every bits
- Magnitude comparator: use subtractor and check the sign bit
### Arithmetic/Logical Unit(ALU)
- Put these together
- Use multiplexer to determine the function
### Shifters and Rotators
- Logical shifter
- Arithmetic shifter: when shift right, keep the most significant bit with origin
- Rotator
- Build with $N$ $N:1$ multiplexers
