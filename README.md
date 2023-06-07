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

## Procedure
The input and output variables are allocated with letter symbols. The exact truth table that defines the required relationships between inputs and outputs is derived. The simplified Boolean function is obtained from each output. The logic diagram is drawn.
## Program:
/*
```
Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by:mathan raj e
RegisterNumber:  212222230079
module cpmbine(a,b,c,d,f);
input a,b,c,d;
output f;
wire p,q,r;
assign p=(~c & b & a);
assign q=(~d & c & c & a);
assign r=(c & ~b & a);
assign f=(~(~p & ~q & ~r));
endmodule

module combine1(a,b,c,d,f);
input a,b,c,d;
output f;
wire p,q,r;
assign p=(c & ~b & a);
assign q=(d & ~c & a);
assign r=(c & ~b & a);
assign f=((p | q & |r));
endmodule
```

*/

## Output:
## RTL
![de exp 2](https://user-images.githubusercontent.com/121418444/232852527-6ab33500-34b7-4ad9-b1d5-fde16b6e1b46.png)
![de exp 2](https://user-images.githubusercontent.com/121418444/232852628-db93882b-2a1b-4b2b-b631-569ec3a069d0.png)

## Timing Diagram
![de exp wf](https://user-images.githubusercontent.com/121418444/232852809-9a8cc8a9-c133-4c3b-accc-b729ce65b987.png)
![de exp wf1](https://user-images.githubusercontent.com/121418444/232853376-c6a75fec-3b98-4ed1-99a8-3c93cc7b8581.png)

## Result:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
