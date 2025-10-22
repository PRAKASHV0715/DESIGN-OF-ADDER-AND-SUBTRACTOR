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

<img width="736" height="561" alt="Screenshot 2025-10-22 115241" src="https://github.com/user-attachments/assets/d5901ca3-bfd0-4a56-b413-238b84dbc8fc" />

<img width="732" height="687" alt="Screenshot 2025-10-22 115302" src="https://github.com/user-attachments/assets/d8c6f432-27a8-4c14-8344-509f4c518067" />

```
**Procedure**
Full Adder:
1.Open Quartus II and create a new project. 2.Use schematic design entry to draw the full adder circuit. 3.The circuitconsists of XOR, AND, and OR gates. 4.Compile the design, verify its functionality through simulation. 5.Implement the design on thetarget device and program it.

Full Subtractor:
1.Follow the same steps as for the full adder. 2.Draw the full subtractor circuit using schematic design. 3.The circuitincludes XOR, AND, OR gates to perform subtraction. 4.Compile, simulate, implement, and program the design similarly to the fulladder.
```
```
**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

// Full Adder in Verilog
module full_adder (
    input  wire a, b, cin,   // Inputs
    output wire sum, carry   // Outputs
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  // XOR for sum
    assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule
```
```
Developed by:PRAKASH V
RegisterNumber:25018527
*/
```
**RTL Schematic**

<img width="714" height="588" alt="Screenshot 2025-10-22 114913" src="https://github.com/user-attachments/assets/49da13c3-1fd3-4b25-b43c-311310ad1c5a" />

**Output Timing Waveform**

<img width="1204" height="252" alt="Screenshot 2025-10-22 114954" src="https://github.com/user-attachments/assets/8387b3c0-bd41-4e20-b773-9bfa9b86a8f7" />

**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



