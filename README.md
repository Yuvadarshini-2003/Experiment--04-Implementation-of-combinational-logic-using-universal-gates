# Experiment--04-Implementation-of-combinational-logic-using-universal-gates
Implementation of combinational logic using universal-gates
 
# AIM:
To implement the given logic function using NAND and NOR gates and to verify its operation in Quartus using Verilog programming.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')' using NAND gate
F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')' using NOR gate

# EQUIPMENTS REQUIRED:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime


# THEORY:
Logic gates are electronic circuits which perform logical functions on one or more inputs to produce one output. 

## Using NAND gates:
NAND gate is actually a combination of two logic gates i.e. AND gate followed by NOT gate. So its output is complement of the output of an AND gate.This gate can have minimum two inputs, output is always one. By using only NAND gates, we can realize all logic functions: AND, OR, NOT, X-OR, X-NOR, NOR. So this gate is also called as universal gate. First note that the entire expression is inverted and we have three terms ANDed. This means that we must use a 3-input NAND gate. Each of the three terms is, itself, a NAND expression. Finally, negated single terms can be generates with a 2-input NAND gate acting as an inverted.

F=((C'.B.A)'(D'.C.A)'(C.B'.A)')'

## Using NOR gates
NOR gate is actually a combination of two logic gates: OR gate followed by NOT gate. So its output is complement of the output of an OR gate. This gate can have minimum two inputs, output is always one. By using only NOR gates, we can realize all logic functions: AND, OR, NOT, Ex-OR, Ex-NOR, NAND. So this gate is also called universal gate. Designing a circuit with NOR gates only uses the same basic techniques as designing a circuit with NAND gates; that is, the application of deMorgan’s theorem. The only difference between NOR gate design and NAND gate design is that the former must eliminate product terms and the later must eliminate sum terms.

F=(((C.B'.A)+(D.C'.A)+(C.B'.A))')'

# PROCEDURE:
## STEP 1:
Create a project with required entities.
## STEP 2:
Create a module along with respective file name.
## STEP 3:
Run the respective programs for the given boolean equations.
## STEP 4:
Run the module and get the respective RTL outputs.
## STEP 5:
Create university program(VWF) for getting timing diagram.
## STEP 6:
Give the respective inputs for timing diagram and obtain the results.

# PROGRAM:
```

Program to implement the given logic function using NAND and NOR gates and to verify its operations in quartus using Verilog programming.
Developed by: Yuvadarshini S
RegisterNumber:212221230126 


using NAND:

   module combo1(a,b,c,d,f);
   input a,b,c,d;
   output f;
   wire p,q,r;
   assign p=(~c & b & a);
   assign q=(~d & c & ~a);
   assign r=(c & ~b & a);
   assign f=(~(~p & ~q & ~r));
   endmodule
   
using NOR:

   module combo2(a,b,c,d,f);
   input a,b,c,d;
   output f;
   wire p,q,r;
   assign p=( c & ~b & a);
   assign q=( d & ~c & a);
   assign r=( c & ~b & a);
   assign f=(~(~( p | q | r)));
   endmodule
```

# OUTPUT:
## USING NAND:
## RTL:
![](1.jpg)
## Timing Diagram:
![](2.jpg)
## Truth table:
![](3.jpg)
## USING NOR
## RTL
![](4.jpg)
## Timing Diagram:
![](5.jpg)
## Truth table:
![](6.jpg)

## RESULT:
Thus the given logic functions are implemented using NAND and NOR gates and their operations are verified using Verilog programming.
