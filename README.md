# Experiment03-Half-Subtractor-and-Full-subtractor
## Implementation-of-Half-subtractor-and-Full-subtractor-circuit
## AIM:
To design a half subtractor and full subtractor circuit and verify its truth table in Quartus using Verilog programming.

## Equipments Required:
 Hardware – PCs, Cyclone II , USB flasher
 Software – Quartus prime
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

```
module fullsub(A,B,Bin,diff,Borrow);
input A,B,Bin;
output diff,Borrow;
assign diff=A^B^Bin;
assign Borrow=(~A&B)|(~(A^B))&Bin;
endmodule
```

# RTL DIAGRAM:

# Half subtracter:

![266497843-95fadd91-9046-4282-85cc-ecc973b65c24](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/24197580-b9cf-4930-a89b-881c0dd7e898)


# Full subtracter:

![266497979-b91e4493-c685-4db8-89db-e4104131ef4c](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/3ffade56-9223-46d6-905c-e54e21f66b8c)


# Truthtable:

HALF SUBTRACTER:

![266499364-248a6bc1-bea5-4720-98aa-d793dfe47254](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/48dd46ab-7638-4b7a-95ee-c020c6bbf69a)


FULL SUBTRACTER:

![266499377-8a487467-cf75-4b40-9dbd-118fbdf6f934](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/c9f9a4ae-ea65-4fbd-820a-cc05b796d71d)


# Output Waveform:

HALF SUBTRACTER:

![266498403-f32a9100-1e29-4929-aaae-947cd6cf8e8f](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/3f051de9-60f7-4326-86a6-38d9306c4986)


FULL SUBTRACTER:

![266500186-0b9b3ae9-9ef4-45c3-98a1-b3e5a7739fda](https://github.com/Yuva2005raj/Experiment--03-Half-Subtractor-and-Full-subtractor/assets/118343998/68293165-134f-4853-86d8-6c23571b1ca1)


RESULT:
Thus the half subtractor and full subtractor circuits are designed and the truth tables is verified using quartus software.
