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
FULL ADDER
<img width="1038" height="583" alt="Screenshot 2025-11-22 095229" src="https://github.com/user-attachments/assets/11a71411-6139-4aa8-830f-f5e4280324af" />

FULL SUBRACTOR
<img width="1032" height="609" alt="Screenshot 2025-11-22 095343" src="https://github.com/user-attachments/assets/9d84f0c3-6d5d-4139-9429-7376494423d0" />



**Procedure**

Write the detailed procedure here

**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by:MONICA R RegisterNumber:25010138
*/
FULLADDER


module experiment4(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule


FULLSUBTRACTOR
module Verilog2(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule




**RTL Schematic**
FULL ADDER

<img width="1901" height="1045" alt="Screenshot 2025-11-22 095830" src="https://github.com/user-attachments/assets/90bfc7fc-3ef6-4322-8099-fff9a63fbfc1" />

FULL SUBRACTOR
<img width="1918" height="1078" alt="image" src="https://github.com/user-attachments/assets/30c12926-0de4-408c-911f-bddf4bef824e" />



**Output Timing Waveform**
FULL ADDER
<img width="1919" height="1079" alt="Screenshot 2025-11-22 100317" src="https://github.com/user-attachments/assets/06d80248-143a-4b71-92a2-6f4ffd4be4ce" />

FULL SUBRACTOR
<img width="1918" height="1076" alt="image" src="https://github.com/user-attachments/assets/9828b2d4-5355-4223-9f29-642a379e2e2b" />




**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



