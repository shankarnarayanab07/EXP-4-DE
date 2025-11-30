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

**Full-Adder**

<img width="593" height="542" alt="Full-Adder TT" src="https://github.com/user-attachments/assets/28bd3fce-b135-4bec-9792-a48f70ff76ce" />

**Full-Subtractor**

<img width="606" height="532" alt="Full-Subtractor TT" src="https://github.com/user-attachments/assets/aeec3cca-2c25-44a0-a3db-e270ca960f81" />


**Procedure**

Type the program in Quartus software.

Compile and run the program.

Generate the RTL schematic and save the logic diagram.

Create nodes for inputs and outputs to generate the timing diagram.

For different input combinations generate the timing diagram.


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: Shankar Narayana B RegisterNumber: 25009078
*/


**Full adder**
```
module exp4(df,bo,a,b,bin);
output df;
output bo;
input a;
input b;
input bin;
wire w1,w2,w3;
assign w1=a^b;
assign w2=(~a&b);
assign w3=(~w1&bin);
assign df=w1^bin;
assign bo=w2|w3;
endmodule

```

**Full subtractor** 
```
module full_subtractor(diff, borrow, a, b, bin);
  output diff;
  output borrow;
  input a;
  input b;
  input bin;
  assign diff = a ^ b ^ bin;
  assign borrow = (a & b) | ((a ^ b) & bin);
endmodule

```

**RTL Schematic**

**Full-Adder**

<img width="1920" height="1200" alt="FA-1" src="https://github.com/user-attachments/assets/4b0d1e76-8258-4885-96cf-9df560b5e098" />

**Full-Subtractor**

<img width="1920" height="1200" alt="FS-1" src="https://github.com/user-attachments/assets/638bebf7-f787-4da3-841d-6aa5f9788943" />




**Output Timing Waveform**

**Full-Adder**

<img width="1920" height="1200" alt="FA-2" src="https://github.com/user-attachments/assets/d6a38ccb-7884-4277-959b-73d84b2bc8ca" />

**Full-Subtractor**

<img width="1920" height="1200" alt="FS-2" src="https://github.com/user-attachments/assets/56dd41ce-aa99-40fa-83ec-3f1570b4e0dd" />



**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



