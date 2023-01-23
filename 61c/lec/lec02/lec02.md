# Binary
**Base:** 2
**Prefix**: `0x`

**Definition**: system of storing data using `1` and `0`, base 2, starts with `0b`

### Memorize
    - Numbers from 1 - 15
    - powers of 2

### Binary SI-prefixes
    - 2 ^ 32 = 2 ^ 30 * 2 ^2
    - (2^10)^3 * 4
    - 4 * (1000)^3

Write binary data as hexadecimal or octal


# Hexadecimal

**Base:** 16
**Prefix**: `0x`

### Converting Hexadecimal to Binary

Base 16 -> 16 = 2^4

convert each digit seperately to binary

split data into sets of 4 digits (prepending to get multiple of 4 digits)

0x14 == 0b10100 == 20

Bases can be written as a subscript

# Representing Data Using Binary

-> Computer sees cluster of wires, high/low voltage wires

-> human needs to assign meaning to binary state, and put together transistors to act equivalently to meaningul operations

Anything put in memory gets stored using some number of bits

Each possible sequence of 1s and 0s (bitstring) can get assigned to at most one meaning

In general, using `n` bits, we can represent up to `2^n` different bitstrings

[Insert Table]

### Example Boolean Valules
    - Two states, `True`, `False`
    - Assign `1` to `True` and `0` to `False`
    - Meaningful operators: OR, AND, NOT, XORA

[Insert Table]

### Example: ASCII
    - no "natural" way to assign bitstrings to characters
    - several options exist to map characters to bits
        - ASCII
    - ASCII
        - each character uses 7 bits of data
        - 2^7 = 128

[Insert Table]

### Padding
    - Don't want to work with 1 bits, but prepend 0's to have 32 bits if needed
    - 8 bit values -> chars

# Binary Mathematics

### Representing Nonnegative Integers

- Solution 1: Treat integer as an array of digits, extending the array as needed to save the entire integer
    - Ex. Decimal numbers in math
    - Ex. Python's large integer primitive
- Solution 2: Only allow for numbers up to a certain max values, using a fixed number of bits
    - Edge Case: math results exceed max values
    - Often referred to as n-bit unsigned integer, allow numbers 0 to 2^n - 1

### Binary Operations

- Common operations: &, |, ^, >>, >>
    - & -> only 1 if both bits are 1
    - | -> 1 if either bit is 1
    - ^ -> 1 if bit is same
    - [add last]
    - >> -> move bits right, add 0's to new places
    - << -> move bits left, add 0's to new places

- first four correspond to AND, OR, NOT, XOR
- Process:
    - convert to binary
    - run process

[insert example]

# Decimal Analogu
    - 1234 <<_10 1 means:
        - move all digits one spot left
        - add zero to end
    - 1234 >> _10 1 means:
        - move all digits one spot right, cutting off last digit
        
### Mathematical operations
    - addition -> same with carry for 1 + 1
    - multiplication -> same
    - Problems:
        - going too high (overflow)
            - 200 + 200
        - going too low (also called overflow)
            - 100 - 200
    - Fractional results -> treat division as floor division
    - take all results $(mod 2^n)$

# Integer Representations
    - Unsigned numbers
        - use mod arithmethic
        - translate into binary
        - used with bitwise operations or when don't need negative numbers
    - Signed Systems
        - have same amount of negative and positive numbers
        - add a bit to represent positive or negative
        - more complex systems
    - Bias Numbers
        - shift numbers
        - Define a "bias"
        - Read data as unsigned number and add bias
        - storing: subtract bias, and store
        - Largest number is, max value - bias
        - used when comparing data
    - Two's Complement Numbers
        - Notice overflow handled by mod 2^n
        - if leading bit is 0, interpret as unsigned
        - if leading bit is 1, interpret number as unsigned and subtract 2^n
        - Result: 2^n's compleent is equivlanet to unsigned value
        - multiply by -1, flip bits and add 1
        
    








