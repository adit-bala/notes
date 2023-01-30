# Endianness, Floating Point Numbers

# Endianness

![storing_values_in_binary](img/storing_values_in_binary.png)

- what happens if we do `((char*) i) [2]`
    - treat i as `char` array, go to second hex byte

![big_end](img/big_end.png)

![little_end](img/little_end.png)

In either case, reading integer yields same result

![big_and_little_end](img/big_and_little_end.png)

- in reality, only flipping to store
- all endiannesses work as long as you are consistent
- C doesn't like converting integers into character arrays
- Big Endian is commonly used in networks (communicating data between networks)
- Little Endian is commonly used within the computer

# Floating Point
- encoding scheme to store arbitrary real numbers
- starts off with a simple structure
    - store relevant values
    - relatively simple circuitry
- start to optimize and becomes complex
    - Denorms, Infinities, Nans

## Goals: What number's do we want to store?
- need to handle:
    - really big numbers (ex. Avogadros' number)
    - really small numbers (ex. Planck's constant)
- Observation:
    - dealing with large numbers, don't care about small absolute differences
- Goal:
    - store number that's accurate within .001%

## Scientific Notation
![sci_notation](img/sci_notation.png)

## Floating Point System: V0

![flo_po_sys](img/flo_po_sys.png)

- store exponent with bias encoding in the order sign-exponent-mantissa
- set to $-(2^{n-1}-1)$

![flo_po_sys_v1](img/flo_po_sys_v1.png)

![flo_po_sys_v1_ex](img/flo_po_sys_v1_ex.png)

![v1_opt1](img/v1_opt1.png)

![v2_formula](img/v2_formula.png)

![prob_underflow](img/prob_underflow.png)

![denorm_numbers](img/denorm_numbers.png)

![v3](img/v3.png)

![v3_example](img/v3_example.png)

## Optimization 2: Dealing with infinity, division by zero

- can still exceed maximum float
- want to include "1/0"

![final_v](img/final_v.png)

![final_v_example](img/final_v_example.png)



