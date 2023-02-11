# RISC-V Instruction Formats

# Lecture 11

## Calling Convention

- After you call a function, you should assume the following
    - all the `t` registers, `a` registers, and `ra` were set to random values
    - all `s` registers stay the same
    - `sp` is the same as before
- Before you return from a function, make sure that:
    - The `sp` and all `s` registers are back to their original value
    - `ra` is set to the value it was when you called the function (remember that `ret` is just `jr ra`!)
    - Your output is in `a0/a1`
    - Your code doesn't use the value of `t0` before setting it

## Overview

- Assembly language is useful because they can be directly translated into binary code
- RV32 -> each instruction is translation to instructions for same length (32 bits long)
- Different instructions require different values
    - "add" specifies 3 register inputs
    - "addi" specifies 2 registers and 1 immediate
- Split 32 bits into "chunks" for each component

## R-Type

![r_type_1](img/r_type_1.png)

![r_type_2](img/r_type_2.png)

![add_example](img/add_example.png)

![step_1](img/step_1.png)

![step_3](img/step_3.png)

![step_4](img/step_4.png)

![s_e_1](img/s_e_1.png)

![s_e_2](img/s_e_2.png)

![s_e_3](img/s_e_3.png)

![r_type_all_instructions](img/r_type_all_instructions.png)

### I-Type

![i_type](img/i_type.png)

![i_type_1](img/i_type_1.png)

![i_type_2](img/i_type_2.png)

![i_type_3](img/i_type_3.png)

## Arithmetic Instructions

![i_type_arithmethic_instructions](img/i_type_arithmethic_instructions.png)

### Load and Jump Instructions

![i_type_l_j](img/i_type_l_j.png)

## S-Type

![s_type](img/s_type.png)

### All Instructions

![s_type_all_instructions](img/s_type_all_instructions.png)
