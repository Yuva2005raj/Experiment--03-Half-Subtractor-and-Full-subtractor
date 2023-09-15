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
![266497488-1405b5b6-d889-4747-be8a-e636fc78e6b9](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/53ee2a7b-e24d-405a-859d-8abc8a1ba29a)

Full subtracter:
![266497557-53f2d536-129c-4e7d-9a78-02338826337a](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/7bf8b66e-913e-4740-a80c-eb78d08837a6)

Waveform:
HALF SUBTRACTER:
![266497889-a2e82798-fb8b-4c9b-8afd-80868d75742f](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/c814cd86-1427-485d-ab4f-4fb74b566e22)

FULL SUBTRACTER:
![266497980-8b8780e8-8821-44e8-bcb6-0f4e6f705981](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/92ae70c7-7c6a-4922-9fe6-24ed53e46f1d)


Truthtable:
HALF SUBTRACTER:
![266497669-8417db91-3f21-4678-8304-8fffa9b37486](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/03e76888-4a95-4e86-91ef-f643b4e787f9)

FULL SUBTRACTER:
![266497753-263a6edf-9b46-41e0-a827-e78a5975d9b8](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/8c58f916-1fef-49ac-9cd8-0572d1d4dff7)

RESULT:

Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
