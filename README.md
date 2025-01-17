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



Write the detailed procedure here 


## Program:
/*
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: S.ANUSHARON

RegisterNumber:  212222240010

1.) For HALF SUBTRACTOR:

module half_sub(a,b,diff,b_out);

input a,b;

wire d;

output diff,b_out;

xor (diff,a,b);

not (d,a);

and (b_out,d,b);

endmodule

2.)For FULL SUBTRACTOR:

module full_sub(b_out,diff,a,b,c_in);

output b_out,diff;

input a,b,c_in;

wire w1,w4,w5,w6;

xor (diff,a,b,c_in);

not (w1,a);

and (w4,w1,b);

and (w5,w1,c_in);

and (w6,b,c_in);

or (b_out,w4,w5,w6);

endmodule

*/

## Output:

## Truthtable

1.for halfsubtractor:

![Screenshot (235)](https://github.com/Anusharonselva/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119405600/4c7943be-42c8-4c94-8175-5bf45267b9cb)

2.For FULL SUBTRACTOR:


![Screenshot (236)](https://github.com/Anusharonselva/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119405600/eee11ba1-bd52-44af-bc72-00910510e7e0)


##  RTL realization

1.for halfsubtractor:


![Screenshot (237)](https://github.com/Anusharonselva/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119405600/aa19b330-d5aa-47e0-a205-9f63cbcc84f4)

2.For FULL SUBTRACTOR:

![Screenshot (238)](https://github.com/Anusharonselva/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119405600/165c4fb2-30bc-459c-a3e4-a89d323b9911)




## Timing diagram 

1.for halfsubtractor:

![Screenshot (239)](https://github.com/Anusharonselva/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119405600/9167020b-bcc7-4e8c-90a8-6b6dcaacef7b)


2.For FULL SUBTRACTOR:

![Screenshot (240)](https://github.com/Anusharonselva/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/119405600/2fe34dcd-fe44-4c4a-8be7-a464d77fb1ee)



## Result:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
