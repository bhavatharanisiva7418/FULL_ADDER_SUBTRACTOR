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

**Procedure**

Full Adder

1. Open Quartus || and create a new project.
2. Use schematic design entry to draw the full adder circuit.
3. The circuit consists of XOR,AND,and OR gates.
4. Compile the design,verify its functionality through simulation.
5. Implement the design ,verify its functionality through simulation.

Full Subtractor

1. Follow the same steps as for the full adder.
2. Draw the full subtractor circuit using schematic design.
3. The circuit includes XOR,AND,OR gates to perform subtraction.
4. Compile,simulate,implement,and program the design similarly to the full adder.


**Program:**

/* Program to design a half subtractor and full subtractor circuit and verify its truth table in quartus using Verilog programming.

Developed by: RegisterNumber:
*/
```
//full adder
module fulladd(sum,cout,a,b,cin);
   output sum;
	output cout;
	input a;
   input b;
   input cin;
  
        //Internal nets
 wire sl,cl,c2;

  //Instantiate logic gate primitives
 xor(sl,a,b);
 and(cl,a,b);
 xor(sum,sl,cin);
 and(c2,sl,cin);
 or(cout,c2,cl);
 endmodule 
 ```

![Screenshot 2024-03-18 084924](https://github.com/bhavatharanisiva7418/FULL_ADDER_SUBTRACTOR/assets/147473922/5c129dee-9a49-4e8f-98db-e21c3f769050)

**RTL Schematic**

![Screenshot 2024-03-18 084939](https://github.com/bhavatharanisiva7418/FULL_ADDER_SUBTRACTOR/assets/147473922/dba24c1f-1a57-447d-b216-9a444fa611b0)


**Output Timing Waveform**

![Screenshot 2024-03-18 085303](https://github.com/bhavatharanisiva7418/FULL_ADDER_SUBTRACTOR/assets/147473922/1e3494d4-52f8-44ac-a274-a25475287386)


**Result:**

Thus the Full Adder and Full Subtractor circuits are designed and the truth tables is verified using Quartus software.



