# FULL_ADDER_SUBTRACTOR

Implementation-of-Full-Adder-and-Full-subtractor-circuit

**AIM:**

To design a Full Adder and Full Subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher

Software – Quartus prime

**Full Adder and Full Subtractor**

**Full Adder**

Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.

Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin 

Carry = AB + ACin + BCin

![437919745-bf0a7383-16c4-40b4-89f5-7f1a37a976ee](https://github.com/user-attachments/assets/cd655a19-3e91-4c6f-b5f8-3757c532576a)


**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![437920294-b6626bf9-62da-4a22-86ac-6e41daf3dd29](https://github.com/user-attachments/assets/9650342e-fe17-46df-8fc5-8e134697f20c)


Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**
## full adder

![Screenshot 2025-04-27 115936](https://github.com/user-attachments/assets/bf0a7383-16c4-40b4-89f5-7f1a37a976ee)

## full subractor

![Screenshot 2025-04-27 120213](https://github.com/user-attachments/assets/b6626bf9-62da-4a22-86ac-6e41daf3dd29)

**Procedure**

**Full Adder:**
1.Open Quartus II and create a new project.

2.Use schematic design entry to draw the full adder circuit. 

3.The circuit consists of XOR, AND, and OR gates. 

4.Compile the design, verify its functionality through simulation. 

5.Implement the design on the target device and program it.

**Full Subtractor:** 
1.Follow the same steps as for the full adder. 

2.Draw the full subtractor circuit using schematic design. 

3.The circuit includes XOR, AND, OR gates to perform subtraction. 

4.Compile, simulate, implement, and program the design similarly to the full adder.

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
## Developed by: Elamaran S E
## RegisterNumber:212222230036
*/

```
module faexp(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule
FULL SUBTRACTOR:
module fsexp(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule

```
**RTL Schematic**

## full adder

![Screenshot 2025-04-27 120446](https://github.com/user-attachments/assets/2b2842a1-7447-44d9-86a5-b619d61685f1)


## full subtractor

![Screenshot 2025-04-27 120525](https://github.com/user-attachments/assets/b1bcf09c-583c-415d-8d19-68a2e1ec47e3)


**Output Timing Waveform**

## full adder

![Screenshot 2025-04-27 120640](https://github.com/user-attachments/assets/03737752-1234-46eb-a8df-1a9803c81cd9)


## full subtractor

![Screenshot 2025-04-27 120654](https://github.com/user-attachments/assets/3d9a2b4c-9554-4bc9-9b92-14bc37da4da7)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
