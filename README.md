# Experiment--02-Implementation-of-combinational-logic
Implementation of combinational logic gates
 
## AIM:
To implement the given logic function verify its operation in Quartus using Verilog programming. F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D F2=xy’z+x’y’z+w’xy+wx’y+wxy Equipments Required: hardware – PCs, Cyclone II , USB flasher Software – Quartus prime

## Theory:
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. Using NAND gates

NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted. F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Logic Diagram:
Using NOR gates NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms. F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

## Procedure:
The input and output variables are allocated with letter symbols. The exact truth table that defines the required relationships between inputs and outputs is derived. The simplified Boolean function is obtained from each output. The logic diagram is drawn. Program:

### Program to implement the given logic function and to verify its operations in quartus using Verilog programming.
```python
Developed by: harithashree.v
RegisterNumber: 212222230046

module combine(a,b,c,d,f);
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
## Output:
## RTL VIEWER:
![image](https://github.com/haritha-venkat/Experiment--02-Implementation-of-combinational-logic-/assets/121285701/8ead6d66-1b73-40a8-9ea9-729047547a3a)
![image](https://github.com/haritha-venkat/Experiment--02-Implementation-of-combinational-logic-/assets/121285701/487bb566-7c53-4c78-b656-9d7db77b7af8)


## TIMING DIAGRAM:
![image](https://github.com/haritha-venkat/Experiment--02-Implementation-of-combinational-logic-/assets/121285701/a992db88-5942-40f3-85c2-cdf9ff827d00)
![image](https://github.com/haritha-venkat/Experiment--02-Implementation-of-combinational-logic-/assets/121285701/5637b966-5411-4127-9072-500fd51c9792)


## RESULT:
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

