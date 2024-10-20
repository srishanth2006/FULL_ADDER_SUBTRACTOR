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
**FULLADDER**
<img width="355" alt="image" src="https://github.com/user-attachments/assets/84ecd12b-851e-494d-89e7-d9b8c7880b74">


**FULL SUBTRACTOR**
<img width="440" alt="image" src="https://github.com/user-attachments/assets/9c88f1bf-16ae-4692-9fc5-6b3afc60ee68">


**Procedure**
```
1. Open Quartus Software   
2. Create a New Project  
3. Create a New Design File  
4. Compile the Program  
5. Generate RTL Schematic  
6. Create Nodes for Inputs/Outputs  
7. Generate Timing Diagram  
8. Simulate Different Input Combinations  
9. Save Your Work  
```

**Program:**
```
Name :SRISHANTH J
Register no:212223240160
```
```
#Full adder
module proj_41(a,b,cin,sum,carry);
input a,b,cin;
output sum, carry;
assign sum=(a^b^cin);
assign carry=((a&b)|(b&cin)|(cin&a));
endmodule

#Full Subtractor
module proj_42(a,b,bin,borr,diff);
input a,b,bin;
output diff, borr;
assign diff=(a^b^bin);
assign borr=((~a&b)|(b&bin)|(bin&~a));
endmodule

```

**RTL Schematic**

#FULL ADDER
<img width="734" alt="image" src="https://github.com/user-attachments/assets/56df3539-a017-496d-bdcc-44b05be5d8c2">

#FULL SUBTRACTOR
<img width="733" alt="image" src="https://github.com/user-attachments/assets/684a1fda-5930-4eb1-a409-16dbd362105b">


**Output Timing Waveform**
#FULL ADDER
<img width="731" alt="image" src="https://github.com/user-attachments/assets/fe555efa-d96a-4aa6-ad94-60f3cc6c23dd">

#Full Subtractor
<img width="733" alt="image" src="https://github.com/user-attachments/assets/55b123d4-6971-49ba-8c8c-f42c896701d8">

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



