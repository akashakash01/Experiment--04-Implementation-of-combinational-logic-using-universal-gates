# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
## AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate
## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime


## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram

Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Logic Diagram
## Procedure
## Program:

Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: AKASH R
RegisterNumber:22008463  
Using NANAD gate
   module exp1(a,b,c,d,f);
   input a,b,c,d;
   output f;
   wire p,q,r;
   assign p=(~c & b & a);
   assign q=(~d & c & ~a);
   assign r=(c & ~b & a);
   assign f=(~(~p & ~q & ~r));
   endmodule
Using NOR gate
   module exp2(a,b,c,d,f);
   input a,b,c,d;
   output f;
   wire p,q,r;
   assign p=( c & ~b & a);
   assign q=( d & ~c & a);
   assign r=( c & ~b & a);
   assign f=(~(~( p | q | r)));
   endmodule
## RTL realization

## Output:
## RTL
![WhatsApp Image 2023-01-19 at 20 39 59](https://user-images.githubusercontent.com/123085535/213481058-ced292b3-83ef-40f9-98dc-8f536d482bd5.jpg)
![WhatsApp Image 2023-01-19 at 20 43 08](https://user-images.githubusercontent.com/123085535/213481120-def2f542-0cc1-4a9e-86b4-6e196b989334.jpg)
![WhatsApp Image 2023-01-19 at 20 41 39](https://user-images.githubusercontent.com/123085535/213481220-8a30b208-cc5f-423e-a26b-6bcafb40c54c.jpg)
![WhatsApp Image 2023-01-19 at 20 44 53](https://user-images.githubusercontent.com/123085535/213481273-d64f362a-44f5-4b42-aa81-874283a748d3.jpg)
![WhatsApp Image 2023-01-19 at 20 40 51](https://user-images.githubusercontent.com/123085535/213481366-599d20e3-699b-4ed0-958b-9cba4bb2a08c.jpg)
![WhatsApp Image 2023-01-19 at 20 44 01](https://user-images.githubusercontent.com/123085535/213481423-609fb512-cd41-4db5-b514-2c36ba4056a7.jpg)

## Timing Diagram
## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
