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

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D

module exp2f1(A,B,C,D,f1);
input A,B,C,D;
output f1;
assign f1=(~B&~D)|(A&B&~C)|(~A&B&D);
endmodule

F2=xy’z+x’y’z+w’xy+wx’y+wxy

module exp2(w,x,y,z,f2);
input w,x,y,z;
output f2;
assign f2=(~y&z)|(x&y)|(w&y);
endmodule
```
## Output:
## RTL VIEWER:
![Screenshot 2023-06-12 142001](https://github.com/haritha-venkat/Experiment--02-Implementation-of-combinational-logic-/assets/121285701/9003cefa-cb8c-43a7-91ec-926f53c1d315)

![Screenshot 2023-06-12 142030](https://github.com/haritha-venkat/Experiment--02-Implementation-of-combinational-logic-/assets/121285701/5ebd6d08-5a6a-434f-ac90-e797154d3b04)


## TIMING DIAGRAM:

![Screenshot 2023-06-12 142105](https://github.com/haritha-venkat/Experiment--02-Implementation-of-combinational-logic-/assets/121285701/3ee3c1b7-7d1c-4c0c-97a9-bf66776fe3c3)

![Screenshot 2023-06-12 142130](https://github.com/haritha-venkat/Experiment--02-Implementation-of-combinational-logic-/assets/121285701/9d874051-9a61-4bba-b35d-fb638b84009c)


## RESULT:
Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

