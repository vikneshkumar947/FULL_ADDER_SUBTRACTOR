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

module ex(a,b,cin,sum,carry);
input a,b,cin;
output sum, carry;
assign sum=(a^b^cin);
assign carry=((a&b)|(b&cin)|(cin&a));
endmodule

Full Subtractor:

module ex2(a,b,bin,borr,diff);
input a,b,bin;
output diff, borr;
assign diff=(a^b^bin);
assign borr=((~a&b)|(b&bin)|(bin&~a));
endmodule
```
**RTL Schematic**
![image](https://github.com/user-attachments/assets/95d563a2-79aa-4bdb-8f16-a902ced91df7)
![image](https://github.com/user-attachments/assets/b2cf3e28-4a5c-47c7-97e0-8f254790ad17)

**Output Timing Waveform**
![image](https://github.com/user-attachments/assets/6e3313d1-05d6-4cc7-b60e-c9a27157a89f)
![image](https://github.com/user-attachments/assets/5dc99e13-1d4d-43f1-9ee2-d2e0bf3ca260)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



