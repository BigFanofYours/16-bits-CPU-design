This is a project about designing a CPU on Quartus to execute custom 16 bits instructions.

The settings for this project should be: 
- Family: Cyclone II
- Package: FBGA
- Pin count: 672
- Speed grade: Fastest
- Device: EP2C35F672C6

Flow of the project:
1. Building the custom instructions: using basic knowledge from Computer Structure's 32-bit MIPS instruction set, implementing and refining it into a 16-bit instruction set with the fields being:

RRR instructions: using 2 registers for operation and 1 as a destination register.
+ Opcode: 3 bits
+ Register 1: 3 bits
+ Register 2: 3 bits
+ Destination register: 3 bits
+ Function: 4 bits

RRI instructions: using 1 register and 1 sign-extended immediate number for calculation, result is stored in destination register.
+ Opcode: 3 bits
+ Register 1: 3 bits
+ Destination register: 3 bits
+ Immediate: 7 bits

RI instructions: using only 1 register for destination and 1 sign-extended immediate number.
+ Opcode: 3 bits
+ Destination register: 3 bits
+ Immediate: 10 bits

2. Designing the actual CPU:
