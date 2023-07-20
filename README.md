# Exp-02 Implementation of Half Adder and Full Adder circuit

# Implementation ofHalf Adder and Full Adder circuit
#### NAME:Nijeesh NJ
#### Register no.: 23010565
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
### Program:

Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.
#### HALF ADDER

module Halfadder(sum,a,b,carry);

input a,b;

output sum,carry;

xor(sum,a,b);

and(carry,a,b);

endmodule 

#### FULL ADDER:

module fulladder(a,b,c,sum,carry);

input a,b,c;

output sum,carry;

xor(sum,a,b,c);

assign carry=a&b | b&c | a&c;

endmodule 

### TRUTH TABLE HALF ADDER:
![image](https://github.com/Nijeesh-bit/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/89188014/ae2d40fe-6869-431b-93b4-1e274bd25771)

### RTL realization HALF ADDER:
![image](https://github.com/Nijeesh-bit/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/89188014/b5171707-bf9a-4e39-9113-ba60af41353b)

### TIMING DIAGRAM HALF ADDER:
![image](https://github.com/Nijeesh-bit/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/89188014/b0ab1794-2348-44c1-997f-56148a344bc4)

### TRUTH TABLE FULL ADDER:
![image](https://github.com/Nijeesh-bit/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/89188014/786927bd-7c2a-4832-8389-da4b876a6ab3)

### RTL realization FULL ADDER:
![image](https://github.com/Nijeesh-bit/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/89188014/4aa2d7c9-f4e6-4739-8181-4ecd4e9c6c6f)

### TIMING DIAGRAM HALF ADDER:
![image](https://github.com/Nijeesh-bit/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/89188014/b3e9c25e-2c1e-4bf1-9561-564710da7214)

### Result:
Thus the given logic functions are implemented using  and their operations are verified using Verilog programming.
