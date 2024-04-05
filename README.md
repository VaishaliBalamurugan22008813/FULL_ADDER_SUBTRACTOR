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

 Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.
 
### FULL_ADDER
```
Developed by: VAISHALI BALAMURUGAN
RegisterNumber: 212222230164
module full_adder(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
wire w1,w2,w3,w4;       
xor(w1,a,b);
xor(sum,w1,cin);        

and(w2,a,b);
and(w3,b,cin);
and(w4,cin,a);

or(carry,w2,w3,w4);
endmodule
```
### FULL_SUBTRACTER
```
Developed by:VAISHALI BALAMURUGAN
RegisterNumber: 212222230164
module full_subtracter(a,b,Bin,BO,DIFF);
input a,b,Bin;
output BO,DIFF;
assign DIFF = a ^ b ^ Bin;
  assign BO = (a & b) | ((a ^ b) & Bin);
endmodule
```

**RTL Schematic**
### FULL_ADDER
![image](https://github.com/SRINIDHISENTHILNATHAN/FULL_ADDER_SUBTRACTOREXP4/assets/121373170/40e08ff5-dd69-43f6-81a2-292c1dc17a78)
### FULL_SUBTRACTER
![image](https://github.com/SRINIDHISENTHILNATHAN/FULL_ADDER_SUBTRACTOREXP4/assets/121373170/18617393-3d4d-40c8-939e-155386d512bd)

**Output Timing Waveform**
### FULL_ADDER
![image](https://github.com/SRINIDHISENTHILNATHAN/FULL_ADDER_SUBTRACTOREXP4/assets/121373170/9c53dee0-25d4-4d74-929c-0086ea109908)
### FULL_SUBTRACTER
![image](https://github.com/SRINIDHISENTHILNATHAN/FULL_ADDER_SUBTRACTOREXP4/assets/121373170/848f8fdb-0d34-4129-b0e6-f6179bb34a6f)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



