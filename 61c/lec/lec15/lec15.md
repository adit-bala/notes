# Combinational Logic

# Truth Tables

![combinational_block](img/combinational_block.png)
- inputs on left, outputs on right
- 4 input function on right

## TT Example #1: 1 iff one (not both) a,b = 1

![xor](img/xor.png)

## TT Example #2: 2-bit adder

![2-bit adder](img/2-bit adder.png)

## TT Example #3: 32-bit unsigned adder

![32-bit unsigned adder](img/32-bit unsigned adder.png)

## TT Example #4: 3-input majority circuit
![3-input](img/3-input.png)
- majority of 1's and 0's

# Logic Gates

### 1/2

![logic_gates_1](img/logic_gates_1.png)

![and_vs_or](img/and_vs_or.png)

- D has a straight line

### 2/2

![logic_gates_2](img/logic_gates_2.png)
- lines for xor don't go through first curved line
- triangle means a buffer
- a == b -> `XNOR`

## 2-input gates extend to n-inputs

![n-input_XOR](img/n-input_XOR.png)

## Truth Table -> Gates (e.g., majority circuit)

![truth_table_gates](img/truth_table_gates.png)

## Truth Table -> Gates (e.g., FSM  circuit)

![fsm_circuit](img/fsm_circuit.png)

# Boolean Algebra

- Power of Boolean Algebra
    - there's a one-to-one correspondence between circuits made up of `AND`, `OR`, and `NOT` gates and equations in BA
    - `+` means `OR`, `*` means `AND`, `!x` means `NOT`

# majority fun

![ba_maj_circ](img/ba_maj_circ.png)

# fsm fun

![ba_fsm_circ](img/ba_fsm_circ.png)

# BA: Circuit & Algebraic Simplification

![circuit simplification](img/circuit simplification.png)
- b + 1 -> 1
    - b or 1 == 1

# Laws of Boolean Algebra

![laws_of_boolean_algebra](img/laws_of_boolean_algebra.png)

# Canonical Forms

## 1

![can_form_1](img/can_form_1.png)

- create expression for every outputted 1

## 2

![can_form_2](img/can_form_2.png)
