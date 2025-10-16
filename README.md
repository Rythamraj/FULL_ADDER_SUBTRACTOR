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
```
Full Adder:
module fa(a,b,cin,sum,carry); 
input a,b,cin; 
output sum,carry; 
assign sum=( (a ^ b)^cin); 
assign carry= ( (a & b)| ( cin &(a ^ b ))); 
endmodule

Full Subtractor:
module fs(a,b,bin,difference,borrow); 
input a,b,bin; 
output difference,borrow; 
assign difference= ( (a ^ b)^bin); 
assign borrow= ( ( a & b)| ( bin & ((a ^ b )))); 
endmodule
```
/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 
Developed by: Rytham Raj RegisterNumber: 25012528

**RTL Schematic**
Full Adder Logic Diagram: [WhatsApp Image 2025-10-16 at 23 09 52_902f5183](https://github.com/user-attachments/assets/1f825150-a732-4e32-956b-63eb8f0cb7c9)
Full Subtractor Logic Diagram: [WhatsApp Image 2025-10-16 at 23 10 12_ecf1fb73](https://github.com/user-attachments/assets/5933feaf-5c7e-491f-b007-f8a5cec79874)

**Output Timing Waveform**
Full Adder Waveform: [WhatsApp Image 2025-10-16 at 23 09 53_077e4074](https://github.com/user-attachments/assets/4cb67295-dd5f-475f-95de-a977e26271e1)
Full Subtractor Waveform: [WhatsApp Image 2025-10-16 at 23 10 13_806ec627](https://github.com/user-attachments/assets/7aa5704b-3528-421f-9cfe-1925b3fd7196)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



