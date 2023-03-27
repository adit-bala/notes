# RISC V Datapath 1

![single-core_processor](img/single-core_processor.png)

- Control -> marionette of the program directing everything, brain
- Datapath -> all the hardware, how to make it all happen, brawn

## Combinational Logic Blocks

![clb](img/clb.png)

![oipcrisvcm](img/oipcrisvcm.png)

- In one clock cycle, execute one instruction (rising edge)
- ex. add, operation gets written at next crack of dawn at rising edge and execution moves for next clock cycle

![ser](img/ser.png)

- stored program idea, program and data both live in memory

![se1](img/se1.png)

![se2](img/se2.png)
- 3 five bit operations for operation, for 2 registers to get data, and 1 register to put data
- data2 gets ignores by mux for i-type instructions

![se3](img/se3.png)

![two_mem](img/two_mem.png)

![ddp](img/ddp.png)

![five_basic_stages](img/five_basic_stages.png)

![image_2023-03-01-10-49-39](img/image_2023-03-01-10-49-39.png)

## Implementing add

![ia](img/ia.png)

![datapath_add](img/datapath_add.png)

![datapath_sub](img/datapath_sub.png)
