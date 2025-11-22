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

#FULL ADDER
```
module Gate_4(
    input  wire a, b, cin,   // Inputs
    output wire sum, carry   // Outputs
);

    // Logic equations
    assign sum   = a ^ b ^ cin;                  // XOR for sum
    assign carry = (a & b) | (b & cin) | (a & cin); // Majority function for carry

endmodule

```

#FULL SUBTRACTOR
```
module Gate_6(
    input  wire a, b, bin,       // Inputs
    output wire diff, borrow     // Outputs
);

    // Logic equations
    assign diff   = a ^ b ^ bin;                  // Difference
    assign borrow = (~a & b) | (~(a ^ b) & bin);  // Borrow logic

endmodule

```

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming. 

Developed by: Srinivas J

RegisterNumber:25015562

**RTL Schematic**
#FULL ADDER

<img width="919" height="654" alt="Screenshot 2025-11-22 203331" src="https://github.com/user-attachments/assets/ebc84330-a4b7-456a-be07-e7de2b268d61" />


#FULL SUBTRACTOR

<img width="924" height="473" alt="Screenshot 2025-11-22 203512" src="https://github.com/user-attachments/assets/f3fb6b7b-3f1c-46a6-afc6-5ffc34f2791b" />


**Output Timing Waveform**
#FULL ADDER

<img width="1245" height="410" alt="Screenshot 2025-11-22 203316" src="https://github.com/user-attachments/assets/545cbcbf-3980-4066-a77e-f6412f11e07f" />


#FULL SUBTRACTOR

<img width="1352" height="354" alt="Screenshot 2025-11-22 203525" src="https://github.com/user-attachments/assets/cca036f3-2e7c-4cc3-9927-636573ec4a2a" />


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



