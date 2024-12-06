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
![Screenshot 2024-12-04 204523](https://github.com/user-attachments/assets/5e8d72b8-e1f8-423f-a66a-990e9099a823)
![Screenshot 2024-12-04 204729](https://github.com/user-attachments/assets/ce213eee-da18-4189-a0c0-28bda95acb97)


**Procedure**

1.Type the program in Quartus software
2.Compile and run the program
3.Generate the RTL schematic and save the logic diagram
4.create nodes for inputs and outputs to generate the timing diagram
5.for different input combinations generate the timing diagram

**Program:**
module ex4(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum=( (a ^ b)^c);
assign carry= ( (a & b)| ( c &(a ^ b )));
endmodule

module ex42(a,b,c,diff,borr);
input a,b,c;
output diff,borr;
assign diff=((a^b)^c);
assign borr=((a&b)|((a^b)&c));
endmodule

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. Developed by: RegisterNumber:
*/

**RTL Schematic**
![Screenshot 2024-12-04 205632](https://github.com/user-attachments/assets/1eed70fb-625f-4b8d-9401-a7b47ebd79d4)
![image](https://github.com/user-attachments/assets/9084b40f-1a3e-4f33-ab2e-b5b255f4aa89)





**Output Timing Waveform**
![Screenshot 2024-12-04 205421](https://github.com/user-attachments/assets/748813ee-1849-4151-be04-870e9e1108cf)

![Screenshot 2024-12-04 204316](https://github.com/user-attachments/assets/62e56355-b03c-423a-9a19-778bbc7f0854)





**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



