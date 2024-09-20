## Pipelining
### Definition
Pipelining is a technique that makes tasks in multiple stages work simultanously, much like in an assembly line. Pipelining can improve CPU performance, making it run more efficiently and increasing the throughput. However, pipelining can introduce hazards such as data, control, and structural hazards, which can stall the pipeline. Techniques like forwarding, branch prediction, and pipeline interlocks are used to minimize these hazards and maintain high performance.
### Stages
- IF(Instruction fetch)
- ID(Instruction decode and register file read)
- EX(Excution or address calculation)
- MEM(Data memory access)
- WB(Write back)
### Pipeline Harzards
#### Structural Harzard
Structural harzard is that when a planned instruction cannot excute in a proper clock cycle because the hardware does not support the combination of instrutions that are set to excute.
#### Data Harzard
Data harzard is that when a planned instruction cannot excute in a proper clock cycle because the needed data are not available yet.
##### Forwarding/Bypassing
A method for resolve data harzard by retrieving the missing data from internal buffers rather than waiting for it to arrive from programmar visable registers or memory.
##### Load-use data harzard
A specific form of data harzard that the data being loaded by a load instrution have not yet become available when they are needed by another instruction.
##### Pipeline stall/Bubble
A stall initiated in order to resolve a harzard.
#### Control Harzard
Control hazards occur when the pipeline makes decisions based on instructions that haven't been fully executed yet, often due to branches or jumps. These hazards arise when the next instruction to execute depends on the outcome of a previous instruction (e.g., a conditional branch). The pipeline may fetch the wrong instructions, leading to wasted cycles when a branch is mispredicted. Techniques like branch prediction, delay slots, and pipeline stalls are used to mitigate control hazards, but they can reduce overall pipeline efficiency by introducing delays while awaiting the correct path.
##### Branch prediction
A method of resolving a branch hazard that assumes a given outcome for the conditional branch and proceeds from that assumption rather than waiting to ascertain the actual outcome.
## Exceptions
### Exception
An unscheduled event that disrupts program execution.
### Interrupt
An exception that comes from outside of the processor.