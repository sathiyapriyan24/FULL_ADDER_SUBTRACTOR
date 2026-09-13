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

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/0f30ba51-5ffb-4198-845f-18e054f675e7)

**Figure -1 FULL ADDER**

**Full Subtractor**

A full subtractor is a combinational circuit that performs subtraction involving three bits, namely minuend, subtrahend, and borrow-in . It accepts three inputs: minuend, subtrahend and a borrow bit and it produces two outputs: difference and borrow.

![image](https://github.com/naavaneetha/FULL_ADDER_SUBTRACTOR/assets/154305477/02b24f51-ab51-4304-9ad6-7b81ffc1ead5)

Diff = A ⊕ B ⊕ Bin 

Borrow out = A'Bin + A'B + BBin

**Truthtable**

**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/
```
module fulladdersub(
   input A, B, Cin,
   output SUM, CARRY, BO, DIFF
);

assign SUM = A ^ B ^ Cin;
assign CARRY = (A & B) | (B & Cin) | (A & Cin);

assign DIFF = A ^ B ^ Cin;
assign BO = (~A & B) | (~A & Cin) | (B & Cin);
endmodule
```
**RTL Schematic**
<img width="1599" height="892" alt="image" src="https://github.com/user-attachments/assets/cda2eb5b-e5d2-4d26-9d2a-a8eb8ccaa229" />

**Output Timing Waveform**
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/85d6c569-20af-491c-bb39-fb180868a520" />

**Result:**
<img width="1600" height="885" alt="image" src="https://github.com/user-attachments/assets/e17801c4-1e3a-435f-9bd7-5fd1c298d6d7" />

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



