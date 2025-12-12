# HALF_ADDER_SUBTRACTOR

Implementation-of-Half-Adder-and-Half Subtractor-circuit

**AIM:**

To design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

**Equipments Required:**

Hardware – PCs, Cyclone II , USB flasher 

Software – Quartus prime Theory Adders are digital circuits that carry out the addition of numbers.

**Half Adder**

Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB

![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/bd4a0b2c-cdbc-4184-ab08-81578f121e1f)

Figure -01 HALF ADDER

**Half Subtractor**

The half-subtractor is a combinational circuit which is used to perform subtraction of two bits. It has two inputs, X (minuend) and Y (subtrahend) and two outputs D (difference) and B (borrow). To perform x - y, we have to check the relative magnitudes of x and y. If x ;;, y, we have three possibilities: 0 - 0 = 0, 1 - 0 = 1, and 1 - I = 0. The result is called the difference bit. If x < y, we have 0 - I, and it is necessary to borrow a 1 from the next higher stage. The I borrowed from the next higher stage adds 2 to the minuend bit, just as in the decimal system a borrow adds 10 to a minuend digit. With the minuend equal to 2, the difference becomes 2 - I = 1. The half-subtractor needs two outputs. One output generates the difference and will be designated by the symbol D. The second output, designated B for borrow, generates the binary signal that informs the next stage that a I has been borrowed. 

Diff = A’B+AB’ =A ⊕ B
Borrow = A’B

 ![image](https://github.com/naavaneetha/HALF_ADDER_SUBTRACTOR/assets/154305477/d76b099c-513f-4e7c-843a-e2fd028a531a)

Figure -02 HALF Subtractor

**Truthtable**

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
// Half Adder in Verilog
module half_adder (
    input  wire a, b,     // Inputs
    output wire sum,      // Sum output
    output wire carry     // Carry output
);

    // Logic equations
    assign sum   = a ^ b;   // XOR for sum
    assign carry = a & b;   // AND for carry

endmodule

// Half Subtractor in Verilog
module half_subtractor (
    input  wire a, b,         // Inputs
    output wire diff, borrow  // Outputs
);

    // Logic equations
    assign diff   = a ^ b;     // XOR for difference
    assign borrow = ~a & b;    // Borrow when a < b

endmodule
```





/* Program to design a half adder and full adder circuit and verify its truth table in quartus using Verilog programming.

Developed by: K.Karankumar RegisterNumber:25017410 */

**RTL Schematic**
# Half_adder #
<img width="670" height="339" alt="Screenshot 2025-12-12 193846" src="https://github.com/user-attachments/assets/ddd9ac1a-4921-4558-a7e7-b93adddda238" />

# Half_subractor #
<img width="952" height="419" alt="Screenshot 2025-12-12 193915" src="https://github.com/user-attachments/assets/3093b66c-73e3-4e04-b82a-c72a24ec02ae" />




**Output/TIMING Waveform**
# Half_adder #
<img width="843" height="254" alt="Screenshot 2025-12-12 193830" src="https://github.com/user-attachments/assets/270d3375-710d-48d6-a368-9d40d7435757" />

# Half_subractor #
<img width="805" height="290" alt="Screenshot 2025-12-12 193801" src="https://github.com/user-attachments/assets/46b61301-bd9b-4bb8-8225-ca944ec12c46" />



**Result:**
      Thus design a half adder and half subtractor circuit and verify its truth table in Quartus using Verilog programming.

