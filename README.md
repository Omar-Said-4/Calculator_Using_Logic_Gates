# Calculator_Using_Logic_Gates![Logic Calculator](https://user-images.githubusercontent.com/87082462/177817414-2189028b-7245-4f61-82a5-521ec9ed4fad.jpeg)
**A 4-bit binary calculator**
1. Remainder (A % B)
2. Addition / Subtraction (A + B) or (A - B) 
3. Multiplication (A * B)
## Remainder
**Extendable Reminder using :**
1. 3 subtractors (3 adders and xor).
2. priority encoder and mux -> for choosing the right value.
3. a nor gate -> for division by zero error.
### Idea
we subtract the A three times and get the value before it becomes negative.
## Addition / Subtraction
**Extendable Adder / Subtractor**
1. adder.
2. 4 muxs -> to choose the complement value or the real value.
3. 2 And gates  / 2 OR gate -> for zero error.
4. 5 Xor gates / 1 OR gate -> to complement the numbers => (two inputs - one output).
### Idea (+-A +- +-B)
- if the input sign negative we convert it to it's 2nd complement.
- the second input sign xor with the operator(+ or -) give the real sign if it.
- we add them using adder.
- if there's a carry out from adder mean that the output negative and it's needed to convert it to it's 2nd complement state.
- if not means that's positive output and it's correct.
## Multiplication
### Extendable Multiplication using :
1. 3 Xor gates -> 1 for sign and the rest for C1, C2.
2. 6 And gates -> to get carries and for C0.
### idea (+-A * +-B)
- the first output is A0.B0.
- the second output is A0.B1 + B0.A1 and carry(C) out.
- the third output is A1.B1 + C and carry(C) out.
- the fourth output is C.
## Main Calculator 
**Uses selectors s1, s2 to select the operation number**
1. 4 muxs -> for o0,o1,o2,sign.
2. And gate -> for o3 =>  as it out from multiplication only.
3. OR/And gates for flags and sign.
4. 7-segment IC converter.
## Teammates
### I worked on this project (software and hardware implementation) with:
- Ali Farid.
- Mahmoud Farid.
- Aliaa Gheis.
