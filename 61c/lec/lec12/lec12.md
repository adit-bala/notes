# RISC-V Instruction Formats

## U-types

![lui](img/lui.png) 

![lui_cornercase](img/lui_cornercase.png)

## AUPIC and Relative Addressing

- `auipc` similarly gets used primarily as a way to save an arbritrary value when used with addi
- main diff is adds result to PC
- instructions involving labels use relative addressing instead of absolute addressingA
![relative_addressing](img/relative_addressing.png)

## U-Type General Instruction

![u_type_general_instruction](img/u_type_general_instruction.png)

![u_all](img/u_all.png)

## Labels

![labels](img/labels.png)

![labels_offsets](img/labels_offsets.png)

## Storing offsets

- all offsets are multiples of 4 -> each instruction takes 4 bytes of memory
- if we store immediate as a signed number, we always have last two bits 0s
- therefore, we don't store the lowest bit of an offset immediate

## B-Type

![b_type](img/b_type.png)
![b_all](img/b_all.png)

## J-Type

![j_type](img/j_type.png)
![j_all](img/j_all.png)

## How to handle immediate large than you can store
![imm_more_store](img/imm_more_store.png)
![b_j_more_store](img/b_j_more_store.png)
