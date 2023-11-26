# Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

 ![image](https://user-images.githubusercontent.com/36288975/163552156-a13e5a56-c638-4110-97d9-8896907c8d25.png)

#### Figure -01 HALF ADDER 


![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

#### Figure -02 FULL ADDER 

### Procedure

Connect the supply (+5V) to the circuit
Switch ON the main switch
If the output is 1, then the led glows.
### 
Program:
/*
Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
Developed by: Sandhiya R
RegisterNumber:  23014146
*/
###Code:
module SANDHIYA(x,y,s,c);
input x,y;
output s,c;
xor(s,x,y);
and(c,x,y);
endmodule

module full_adder(x, y, z, s, c, x1, x2, x3);
input x,  y,z;
output s ,c, x1, x2, x3;
xor(x1, x, y);
xor(s, x1, z);
and(x2, x, y);
and(x3, x1, z);
or(c, x2, x3);
endmodule

### Output:
### RTL
Half adder:

![image](https://github.com/SandhiyaRajagopal/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870852/c9c29bf9-f41a-4e93-a35e-7745e992f48a)


Full adder:

![image](https://github.com/SandhiyaRajagopal/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870852/83b3ac33-0f30-420c-b7ef-f42dac4710f7)


### TIMING DIAGRAM
Half adder:

![image](https://github.com/SandhiyaRajagopal/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870852/99bc3527-404b-447b-8487-119491dcb452)


Full adder:

![image](https://github.com/SandhiyaRajagopal/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870852/77272663-1cf8-4df0-8225-ebd0166efcc8)

### TRUTH TABLE 

Half adder:

![image](https://github.com/SandhiyaRajagopal/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870852/b1e36a28-ec84-4a81-892f-abd3068a3506)


Full adder:

![image](https://github.com/SandhiyaRajagopal/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/144870852/c62426fb-2720-4842-9c7a-25c6f0bf9aea)


### Result:Thus the half adder and full adder circuit are designed and the truth table for half adder and full adder are verified.
