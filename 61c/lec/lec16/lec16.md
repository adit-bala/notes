# Introduction to Synchronous Digital Systems (SDS) State

## Accumulator

### Uses for State Elements

- A place to store values for some indeterminate amount of time
    - Register files (like x0-x31 on the RISC-V)
    - Memory (cahces, and main memory)
- Help control the flow of information between combinational logic blocks
    - State eleemnts are used to hold up the movement of information tat the inputs to combinational logic blocks and allow for orderly passage.

## Accumulator Example

![ae](img/ae.png)

## First Try

![ft](img/ft.png)

## Second Try

![st](img/st.png)

# Register Details Flip-flops
## Register Details...What's inside?
![rd_wi...](img/rd_wi....png)

## timing of a flip-flop
![tff](img/tff.png)
- clock is consistent
- checks to see if d is rising edge when clock is rising edge

## timing of a flip-flop 2
![tff2](img/tff2.png)
- input needs to be stable for +/- margin before rising edge
- time before rising edge is called set up time, d should be stable
- time after rising edge is called hold time, d should be stable
- "clk-to-q" delay time for how long hold time is

## Accumulator Revisited 1/2

![ar1](img/ar1.png)

## Accumulator Revisited 2/2

![ar2](img/ar2.png)
- if reset is high ignore other outputs
- output becomes 0 after clk-q-delay
- $X_i$ add to $S_i - 1$ to become $S_i$

# Pipelining for Performance
## Maximum Clock Frequency

![mcf](img/mcf.png)

## Pipelining to improve performance 1

![pip1](img/pip1.png)

![pip2](img/pip2.png)

## Recap of Timing Terms

![rtt](img/rtt.png)

## Finite State Machines

![fsm_intro](img/fsm_intro.png)

### Examples

![image_2023-02-24-10-49-25](img/image_2023-02-24-10-49-25.png)

### Hardware implementations

![hardware_implementation_fsm](img/hardware_implementation_fsm.png)

![cl](img/cl.png)

## General Model for Synchrnonous Systems

![gmss](img/gmss.png)

## Design Hierarchy

![dh](img/dh.png)
