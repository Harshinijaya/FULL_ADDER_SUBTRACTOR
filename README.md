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
module exp_3a(A,B,C,sum,carry);
input A,B,C;
output sum,carry;
assign sum=A^B^C;
assign carry=((A&B)|(A&C)|(B&C));
endmodule

FULL SUBTRACTOR:
module exp_3b(A,B,C,dif,bor);
input A,B,C;
output dif,bor;
assign dif=A^B^C;
assign bor=(~A&C)|(~A&B)|(B&C);
endmodule
```
**RTL Schematic**
FULL ADDER:
<img width="1920" height="1080" alt="Screenshot 2026-03-10 093516" src="https://github.com/user-attachments/assets/bedcf5bb-f90e-40eb-a277-f3822583e074" />

FULL SUBRACTOR:
<img width="1920" height="1080" alt="Screenshot 2026-03-10 094544" src="https://github.com/user-attachments/assets/e68f8745-34ec-4f3b-b1dc-cd7cc23c1b94" />


**Output Timing Waveform**
FULL ADDER:
<img width="1920" height="1080" alt="Screenshot 2026-03-10 094356" src="https://github.com/user-attachments/assets/8490a404-5411-4dc6-b1c8-e5ede2e77d1a" />
FULL SUBRACTOR:
<img width="1920" height="1080" alt="Screenshot 2026-03-10 094758" src="https://github.com/user-attachments/assets/1fc71f74-883b-4c6e-b435-bc4d87ce1a6a" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



