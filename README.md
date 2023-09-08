
## Developed by: LATHISH KANNA.M
## RegisterNumber:  212222230073


# Experiment 04 Half Subtractor and Full subtractor
## Implementation of Half subtractor and Full subtractor circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
## Hardware – PCs, Cyclone II , USB flasher
## Software – Quartus prime
## Theory
Subtractor circuits take two binary numbers as input and subtract one binary number input from the other binary number input. Similar to adders, it gives out two outputs, difference and borrow (carry-in the case of Adder). There are two types of subtractors.

## Half Subtractor Full Subtractor
## Half Subtractor
The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed.
![half-subtractor9](https://user-images.githubusercontent.com/36288975/166112538-58c3bc7c-ee5d-4e6a-ac8d-8e8328efe27a.png)


Sum = X'Y+XY' = X ⊕ Y
Carry=X'Y

## Full Subtractor
A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow. 
![full-subtractor6](https://user-images.githubusercontent.com/36288975/166112541-24c68359-3de8-4674-ae22-8272ffc385ed.png)


Diff = A ⊕ B ⊕ Bin B = A'Bin + A'B + BBin

## Procedure

1.Use module projname(input,output) to start the Verilog programmming.

2.Assign inputs and outputs using the word input and output respectively.

3.Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

4.Use each output to represnt onre for differnce and the other for borrow.

5.End the verilog program using keyword endmodule.


Write the detailed procedure here 


## Program:
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
```
Half subtractor:

module ex4(A,B,Difference,Borrow);
input A,B;
output Difference,Borrow;
assign Difference=(A^B);
assign Borrow=(~A&B);
endmodule 

Full subtractor:

module exp4(A,B,Bin,Difference,Borrow);
input A,B,Bin;
output Difference,Borrow;
assign Borrow=((~A)&B)| ((~(A^B))&Bin);
assign Difference=(A^B^Bin);
endmodule

```
## Truthtable:

## Half subtractor:

![image](https://github.com/Pavithraramasaamy/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118596964/b96990dd-e9c5-43e9-9649-4258069ae83a)

## Full subtractor:

![image](https://github.com/Pavithraramasaamy/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118596964/f11c293e-9f11-4fb4-92f8-d4465af1d3e5)

##  RTL realization

## Half subtractor:

![exp4 hr](https://github.com/Pavithraramasaamy/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118596964/82829837-d41e-4396-80fe-6de88046201b)

## Full subtractor:


![exp4 fr](https://github.com/Pavithraramasaamy/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118596964/4cf013af-ea74-446f-a1a8-08f5025d8bd9)



## Timing diagram :

## Half subtractor:


![exp4 hg](https://github.com/Pavithraramasaamy/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118596964/9c69a43a-0104-4ab7-b88d-8a065fcb78ec)


## Full subtractor:

![exp4 fg](https://github.com/Pavithraramasaamy/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118596964/991c237f-8fc9-4b51-b2c5-9c3f17c7f52f)

## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
