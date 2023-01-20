# Lecture 01: Intro

## Great Ideas

### 1: Abstraction (Layers of Representation and Interpretation)

```python

x = 3
x = len

# anything can be a python name
```

Anything can become a number in hardware.

### 2: Moore's Law - 2005

Predicted 2x transistors/chip every 2 years. Moore's Law begins to taper off in recent years

### 3: Principle of Locality / Memory Hierarchy

> Storage Latency Analogy -> How Far Away is the Data?
Depending on where we leave data, we need to go further to fetch it. 

Closest to Furthest
1. CPU Core
2. Registers
3. Cache
4. Physical Memory
5. RAM
6. Virtual Memory
7. Solid-State Memory
8. Magnetic Disks

### 4: Parallelism

#### (1/3)
> Instruction-Level Parallelism -
In different time cycles, multiple instructions can be executed

Process:
1. Instruction Fetch
2. Instruction Decode
3. Execute
4. Memory Access
5. Write Back

#### (2/3)

> Thread-Level Parallelism -
Different work in different threads

#### (3/3)

> Data-Level Parallelism -
Synonymous to splitting up work and merging it together

**Caveat - Amdahl's Law**
> Performance gains are limited by the ratio of software processing that must be executed sequentially

#### 5: Performance Measurement & Improvement

We will focus on Latency/Throughput:
- How long to set the problem up and complete it
- How much faster does it execute once it gets going

#### 6: Dependability via Redundancy

