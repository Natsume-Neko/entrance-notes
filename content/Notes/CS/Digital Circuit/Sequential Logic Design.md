## Latches and Flip-Flops
### SR Latch
#### Schematic
Note that we can build it in other ways, as long as maintain the truth table.
![[SRLatchSchematic.png]]
#### Truth Table
- S: set
- R: reset
![[SRLatchTruthTable.png]]
#### Symbol
![[SRLatchSymbol.png]]
### D Latch
#### Figures
![[D Latch.png]]
#### Explanation
CLK stands for clock and D stands for data input. When CLK=0, D latch blocks the data input from D and keeps previous value. When CLK=1, D latch works transparently that acts like a buffer tansfer the data input from D to Q.
### D Flip-Flop
#### Figures
![[D Flip-Flop.png]]
#### Explanation
The output Q of D flip-flop copies data input D only when CLK change from 0 to 1(in other words, the rising edge), and remember the previous state in any other times.
### Registers
An N-bit register is a bank of N flip-flops that share a common CLK.
### Enabled Flip-Flop
#### Figures
![[Enabled Flip-Flop.png]]
#### Explanation
When EN=1, it works like D flip-flop. When EN=0, Q remembers the state and ignores the CLK. Note that (b) schematic will face a clock glitch when EN changes while CLK=1.
### Resettable Flip-Flop
#### Figures
![[Resettable Flip-Flop.png]]
#### Explanation
When RESET=0, it works like an ordinary D flip-flop. When RESET=1, it resets Q to 0 and ignores D. The figure above display the synchronously resettable flip-flop, which resets Q only at rising edge. Asynchronously resettable flip-flop will ignore the CLK and reset Q to 0.
## Synchronous Sequential Circuit
### Definition
- Only contain registers and combinational circuits
- At least one register
- Every cyclic path must contain at least one register
- All register receive the same clock signal
## Finite State Machines
### State Encoding
- Binary encoding
- One-hot encoding
