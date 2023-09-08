# Experiment03-Half-Subtractor-and-Full-subtractor
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
1..Create a project with required entities.

2.Create a module along with respective file name.

3.Run the respective programs for the given boolean equations.

4.Run the module and get the respective RTL outputs.

5.Create university program(VWF) for getting timing diagram.

6.Give the respective inputs for timing diagram and obtain the results.



## Program:
```
Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
Developed by: YUVARAJ B
RegisterNumber: 212222230182
```

## HALF SUBTRACTER:
```
module halfsubtractor(A,B,diff,borrow);
input A,B;
output diff,borrow;
assign diff=A^B;
assign borrow=~A&B;
endmodule
```

## FULL SUBTRACTER:
````
module fullsub(A,B,Bin,diff,Borrow);
input A,B,Bin;
output diff,Borrow;
assign diff=A^B^Bin;
assign Borrow=(~A&B)|(~(A^B))&Bin;
endmodule
```
RTL DIAGRAM:

Half subtracter:

![266495897-94f0de39-977d-458f-9942-f6ced47c3fde](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/f521f686-da7a-4677-94f0-1f2f39a2fe06)

Full subtracter:

![266495938-a934b87e-c590-4abf-9375-5890b6b73f87](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/ac3be682-0162-466e-8dd6-e2ad42a495ee)

Waveform:

HALF SUBTRACTER:

![266496048-fba3c7ad-df50-47d3-963f-466d22e7ae10](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/3d4d7c80-e763-4c74-99f0-1482fea45177)

FULL SUBTRACTER:

![266496091-9284c59d-31a5-4fd9-81b6-9d2e36aa5088](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/86018b84-a3c1-4b8d-8c1a-aa45e87d9e0b)

## Truthtable

HALF SUBTRACTER:
![266497592-45393802-6f3b-4862-8527-32ac7e089236](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/c1d8a6fe-65dd-42ec-88e2-f62a1c888e7c)

FULL SUBTRACTER:

![266496839-97c26b6f-9aa5-418e-ba5c-13dee3f02ad9](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/5c6f568d-687b-4f29-8172-c22ac468d5b3)

RESULT:

Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
