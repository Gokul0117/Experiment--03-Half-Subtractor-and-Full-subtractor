# Experiment--03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
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

## STEP 1:

Use module project name(input,output) to start the Verilog programmming.

## STEP 2: 

Assign inputs and outputs using the word input and output respectively.

## STEP 3:

Use defined keywords like wire,assign and required logic gates to represent the boolean expression.

## STEP 4: 

Use each output to represnt onre for differnce and the other for borrow.

## STEP 5: 

End the verilog program using keyword endmodule.


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by:Gokul J
RegisterNumber:212222230038

HALF SUBTRACTOR  

module HS(a,b,diff,borr);
input a,b;
output diff,borr;
assign diff=(a^b);
assign borr=(~a&b);
endmodule  


FULL SUBTRACTOR  

module FS(a,b,c,diff,borr);
input a,b;
output diff,borr;
assign diff=(a^b^c);
assign borr=(~a&(b^c)|(b&c));
endmodule  

*/

## Output:

## Truthtable

HALF SUBTRACTOR
![Screenshot 2023-04-23 214345](https://user-images.githubusercontent.com/121165938/233851513-c4cfd6fc-82f0-448b-b779-8e460348aa10.png)

FULL SUBTRACTOR
![Screenshot 2023-04-23 214403](https://user-images.githubusercontent.com/121165938/233851533-a8afb37e-2797-469b-9c6b-2e3d8c738cb4.png)




##  RTL realization

HALF SUBTRACTOR
![Screenshot 2023-04-23 214427](https://user-images.githubusercontent.com/121165938/233851603-0c278bf5-74df-421a-b034-31543aeb97a1.png)

FULL SUBTRACTOR
![Screenshot 2023-04-23 214445](https://user-images.githubusercontent.com/121165938/233851627-d753ee3e-2ddf-4385-9600-dd254e579dc2.png)



## Timing diagram 

HALF SUBTRACTOR
![Screenshot 2023-04-23 214516](https://user-images.githubusercontent.com/121165938/233851656-4f1f0b93-6c41-4a85-b10e-35b80166a3e4.png)

FULL SUBTRACTOR
![Screenshot 2023-04-23 214537](https://user-images.githubusercontent.com/121165938/233851674-838dd04c-fb84-478b-a144-582d6e318f97.png)


## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
