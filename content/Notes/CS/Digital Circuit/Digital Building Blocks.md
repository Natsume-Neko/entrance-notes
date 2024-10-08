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
- $A - B = A + \bar{B} + 1$
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
## Sequential Building Blocks
### Counters
An $N$-bit binary counter has clock and reset inputs and an $N$-bit output. Each time at rising edge, the output will increment by 1. And when reset is asserted, the output will be reset to 0. They can implemented with an $N$-bit resettable register and an $N$-bit adder.
### Shift Registers
A shift register has a serial input $S_{in}$, a serial output $S_{out}$ and an $N$-bit parallel output $Q_{N-1:0}$. At every rising edge, a new bit is shifted in from $S_{in}$ and all the subsequent contents are shifted forward. $S_{out}$ is the last available bit.
Related circuit: parallel to serial converter. (It has parallel load, when load is asserted, the output will change to the load. In other time, it works just like a common shift register.)
## Memory Arrays
- RAM: DRAM, SRAM
- ROM
## Logic Arrays
- PLA
- FPGA
