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
![image](https://github.com/user-attachments/assets/9a97c220-88a1-4e57-92d6-458bbd9c3988)
![image](https://github.com/user-attachments/assets/628cfbe8-e4ca-47f8-94b4-8e9a2af3dc18)

**Output Timing Waveform**
![image](https://github.com/user-attachments/assets/d8afca44-260b-48c7-b57d-532a40139d42)
![image](https://github.com/user-attachments/assets/398d7f96-967b-4d89-ac2f-517edbdb1ee0)

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



