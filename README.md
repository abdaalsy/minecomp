# Minecraft Computer
Hello! This repository contains the world folder, and some instructions to get you up and and running with the Minecraft computer.

![Demo video](./fibonacci.gif)

_Generating the fibonacci sequence in hexadecimal form until 233 (forgot to display the first two terms, significantly sped up)_

## Specs
Clock frequency: slow

RAM: 128 Bytes

## Writing a Program
### Registers
You may have read this term but don't yet understand the meaning. A register is simply a storage element. They are like variables, in that you can store any 8-bit value in them. This computer provides 4 registers for you to use. I gave them labels `r0`, `r1`, `r2`, and `r3`, but you are free to use whatever you want since this computer does not take textual code. Just try not to get mixed up between the numbers. 

### The Program Counter
This is a special register which stores the RAM address of the next instruction to perform. When the computer starts up, the program counter starts at 0, and increments by 3 at each `fetch` of the fetch-execute cycl.

### The Instruction Set
The first step towards getting something running on the computer is to write the program in assembly. Later on when we actually load the program in the computer's memory, this will make it easier to pick the correct binary pattern for an instruction.

The instruction set provides 14 different instructions, many of which can optionally take in an immediate value (a value inputted literally). Here are the available choices:
Note: `rb/immediate` means that you can either use a register or an immediate for this operand.

- `SLL ra rb/immediate rc` - Bit shift `ra` to the left by `rb/immediate` bits, store output in `rc`
- `ADD ra rb/immediate rc` - Adds `ra` and `rb/immediate`, stores the sum in `rc`
- `SUB ra rb/immediate rc` - Same thing as ADD except it subtracts
- `XOR ra rb/immediate rc` - Bitwise XOR between `ra` and `rb/immediate`, store the result in `rc`
- `OR ra rb/immediate rc` - Bitwise OR between `ra` and `rb/immediate`, store the result in `rc`
- `AND ra rb/immediate rc` - Bitwise AND between `ra` and `rb/immediate`, store the result in `rc`
- `SRL ra rb/immediate rc` - Bit shift `ra` to the right by `rb/immediate` bits, store output in `rc`
- `STORE ra rb/immediate` - Stores in the RAM address of `ra`, the value of `rb/immediate` 
- `LOAD ra rb` - Reads the value stored at the RAM address of `ra` into `rb`
- `BEQ ra rb immediate` - Adds `immediate` to the program counter if `ra` and `rb` are equal, otherwise we proceed regularly. (Or in other words, branch if equal).
- `BLT ra rb immediate` - Branch if less than
- `BGT ra rb immediate` - Branch if greater than
- `JMP immediate` - Adds `immediate` to the program counter always (it must be an immediate value).

## Loading a Program
### How the Computer takes in instructions
### Encoding an instruction in binary
### Encoding operands in binary
### Writing to the Computer's Memory

## Running a Program
### The OFF/ON switch
### Starting the clock
### The PAUSE switch
### The 7 segment display
