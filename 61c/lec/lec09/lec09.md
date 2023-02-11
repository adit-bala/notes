# RISC-V Decision Making and Logical Operators

## Review 
- Memory is byte-addressable, but `lw` and `sw` access one word at a time
- Pointer (used by `lw` and `sw`) is just a memory address, can add and subtract to it (w/ offset)
- Big vs Little Endian
    - draw lowest byte on the right
- New Instructions:
    - `lw, sw, lb, sb, lbu`
- don't need to expand when storing (no `sbu`)

## RV32 so far

![rv32_so_far](img/rv32_so_far.png)

## Computer Decision Making

- Based on computation, do something different
- `if` statements
    - `beq reg1, reg2, L1`
    - go to statement labeled `L1 if (value in reg1) == (value in reg2)`
    - ...otherwise, go to next statement
    - `beq` stands for *branch if equal* (`if`)
    - Other instruction: `bne` for *branch if not equal* (`else`)

## Types of Branches

- Branch - change of control flow
    - `beq` -> if equal
    - `bne` -> if not equal
    - `blt` -> if less than
    - `bge` -> if greater than
    - unsigned versions (`bltu`, `bgeu`)
- Unconditional Branch - always branch
    - `j` -> jump 
        - `j label`
## Example *if-else* statement

![example_if_else](img/example_if_else.png)

#### Take away

- might need to negate conditions to show equality (C: `i == j`, RV: `bne x__, x__`)

## Magnitude Compares in RISC-V

![magnitude_compares_risc-v](img/magnitude_compares_risc-v.png)

## Loops in C/Assembly

- three types
    - `while`
    - `do ... while`
    - `for`
- each can be written as either of the other two, so same branching method can be applies to loops
- **Key**: Though there are multiple ways of writing a loop in RISC-V, the key to decision-making is conditional branch

## C Loop Mapped to RISC-V Assembly

![c_loop_rv_assembly](img/c_loop_rv_assembly.png)

- steps
    1. get pointer to array in memory
    2. init sum
    3. get `i` counter
    4. get length (20)
    5. loop

## Logical Instructions

![rv_sofar](img/rv_sofar.png)

![logical_instructions](img/logical_instructions.png)

![variants_in_immediate](img/variants_in_immediate.png)

![no_not_in_rv](img/no_not_in_rv.png)

## Logical Shifting

![logical_shifting](img/logical_shifting.png)

## Arithmetic Shifting

![arithmetic_shifting](img/arithmetic_shifting.png)

## Helpful RISC-V Assembler Features

![assembler_features](img/assembler_features.png)
