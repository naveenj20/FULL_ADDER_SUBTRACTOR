# DATE : 19/03/2025

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

![Screenshot 2025-04-15 114048](https://github.com/user-attachments/assets/35e89dfd-ed0e-4976-a5d1-55fcadf38c6d)


**Procedure**

**Full Adder:**  
1. Launch Quartus II and start a new project.  
2. Use the schematic editor to design the full adder circuit.  
3. Construct the circuit using XOR, AND, and OR logic gates.  
4. Compile the project and verify its operation through simulation.  
5. Upload the design to the target hardware and program the device.

**Full Subtractor:**  
1. Repeat the initial steps as done for the full adder.  
2. Design the full subtractor circuit using the schematic editor.  
3. Use XOR, AND, and OR gates to build the subtraction logic.  
4. Compile, simulate, and program the design just like the full adder.

**Program:**

```
#full_adder
module FULL_ADDER(a,b,cin,sum,carry);
input a,b,cin;
output sum,carry;
assign sum=( (a ^ b)^cin);
assign carry= ( (a & b)| ( cin &(a ^ b )));
endmodule

#full_subtractor
module FULL_SUBTRACTOR(a,b,bin,difference,borrow);
input a,b,bin;
output difference,borrow;
assign difference= ( (a ^ b)^bin);
assign borrow= ( ( ~a & b)| ( bin & (~(a ^ b ))));
endmodule
```

Developed by: Naveen Jaisanker
Register No.: 212224110039

**RTL Schematic**

![Screenshot 2025-04-15 113444](https://github.com/user-attachments/assets/ef2f19cc-fa41-47b9-a5e7-2dd0d16390c9)

![Screenshot 2025-04-15 113854](https://github.com/user-attachments/assets/70309559-bb5e-4739-819d-472a15371b9a)

**Output Timing Waveform**

![Screenshot 2025-04-15 113729](https://github.com/user-attachments/assets/187daa66-095a-44ff-afa5-d6a485dc76a7)

![Screenshot 2025-04-15 113938](https://github.com/user-attachments/assets/dae2767e-9b4e-4254-b087-439b1a23cf27)

**Result:**

Thus, the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.
