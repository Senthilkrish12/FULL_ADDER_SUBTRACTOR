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
![Screenshot 2024-12-03 084951](https://github.com/user-attachments/assets/b5503988-febf-45f6-ad30-e2ceb5a965b4)

FULL SUBTRACTOR:
![Screenshot 2024-12-03 085129](https://github.com/user-attachments/assets/871e08c6-0069-442d-96e6-fad712715614)

**Procedure**
1. Type the program in Quartus software.
2. Compile and run the program.
3. Generate the RTL schematic and save the logic diagram.
4. Create nodes for inputs and outputs to generate the timing diagram.
5. For different input combinations generate the timing diagram.
\

### **Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: Senthil Raj G
RegisterNumber: 212224100054

```
module fulladddataflow(a, b, cin, sum, carry); 
  input a; 
  input b;
  input cin; 
    output sum; 
    output carry; 
 assign sum=a^b^cin; 
 assign carry=(a & b) | (b & cin) | (cin & a); 
 endmodule
```
```
module fulsubdataflow(a, b, cin, diff, borrow); 
    input a; 
    input b; 
    input cin; 
    output diff; 
    output borrow; 
  wire abar; 
  assign abar= ~ a; 
  assign diff=a^b^cin; 
  assign borrow=(abar & b) | (b & cin) |(cin & abar); 
endmodule
```
*/

**RTL Schematic**
FULL ADDER: 
![Screenshot 2025-04-15 201534](https://github.com/user-attachments/assets/1df6f165-560f-45ab-96b4-5f2e20a609a8)


FULL SUBTRACTOR: 
![Screenshot 2025-04-15 201628](https://github.com/user-attachments/assets/427586cf-ea92-42e4-9100-9ccb5158bc77)


**Output Timing Waveform**
![Screenshot 2025-04-15 201713](https://github.com/user-attachments/assets/8aea8a07-f9bb-42e1-816f-14571da51881)
![Screenshot 2025-04-15 201732](https://github.com/user-attachments/assets/19fd8280-cb90-4f48-ba4b-a0cd9391ea5d)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
