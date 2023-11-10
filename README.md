# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming.
 F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D
F2=xy’z+x’y’z+w’xy+wx’y+wxy
 
## Equipments Required:

Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime




## Theory
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

1.AND gate The AND gate is an electronic circuit that gives a high output (1) only if all its inputs are high. 
  A dot (.) is used to show the AND operation i.e. A.B or can be written as AB Y= A.B

2.OR gate The OR gate is an electronic circuit that gives a high output (1) if one or more of its inputs are high. 
  A plus (+) is used to show the OR operation. Y= A+B

## Procedure
1.Use module projname(input,output) to start the Verilog programmming.
2.Assign inputs and outputs using the word input and output respectively.
3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.
4.Use each output to represent one for F1 and the other for F2.
5.End the verilog program using keyword endmodule.
## Program:
```python

Program to implement the given logic function and to verify its operations in quartus
using Verilog programming.
Developed by: MITHUN MS
RegisterNumber: 212222240067


F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

module imp(A,B,C,D,F1);
input A,B,C,D;
output F1;
wire p,q,r,s,t;
assign p = (~A & ~B & ~C & ~D);
assign q = (A & ~C & ~D);
assign r = (~B & C & ~D);
assign s = (~A & B & C & D);
assign t = (B & ~C & D);
assign F1 = p | q | r | s | t;
endmodule

F2=xy’z+x’y’z+w’xy+wx’y+wxy

module imp(w,x,y,z,F2);
input w,x,y,z;
output F2;
wire p,q,r,s,t;
assign p= (x & ~y & z);
assign q= (~x & ~y & z);
assign r= (~w & x & y);
assign s= (w & ~x & y);
assign t= (w & x & y);
assign F2= p | q | r | s | t;
endmodule
```
## RTL realization

## Output:
### Logical Diagram:
![logical diagram](https://github.com/Aakashraj04/Experiment--02-Implementation-of-combinational-logic-/assets/121117266/230f5b7c-264b-49dd-81aa-bedcfb1b3983)

## RTL realization
#### For F1
![f1](https://github.com/Aakashraj04/Experiment--02-Implementation-of-combinational-logic-/assets/121117266/33bf1982-c9f4-4e82-a293-ac0348beb82a)


#### For F2
![f2](https://github.com/Aakashraj04/Experiment--02-Implementation-of-combinational-logic-/assets/121117266/e3f57368-7e81-4a4d-a6c6-cdbb09357123)


## Timing Diagram
#### For F1
![f1 t](https://github.com/Aakashraj04/Experiment--02-Implementation-of-combinational-logic-/assets/121117266/de7ae561-f974-4f04-aa9a-420aff741d78)


#### For F2
![f2 t](https://github.com/Aakashraj04/Experiment--02-Implementation-of-combinational-logic-/assets/121117266/0fa16d6e-e4ff-43e2-be8e-bc2d1d6d8b3f)


## Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
