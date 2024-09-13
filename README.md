# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flashe

**Theory**

Phone number validation involves checking the input string against a set of rules. We'll implement a basic validation logic using Finite State Machine (FSM) and digital electronics concepts:

Finite State Machine (FSM): FSM is a digital circuit that can be in one of a finite number of states.
Moore Machine: A Moore machine is a type of FSM where the output depends only on the current state.
Mealy Machine: A Mealy machine is a type of FSM where the output depends on both the current state and input.

**Procedure**

1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.


**Program:**
```
/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 

Developed by:P G KUSHALI
RegisterNumber:212223230110
*/

module EXP2(A,B,C,D,W,X,Y,Z,F1,F2);
input A,B,C,D,W,X,Y,Z;
wire x1,x2,x3,x4,x5,x6,x7,x8,x9,x10;
output F1,F2;
assign x1=(~A)&(~B)&(~C)&(~D);
assign x2=(A)&(~C)&(~D);
assign x3=(~B)&(C)&(~D);
assign x4=(~A)&(B)&(C)&(D);
assign x5=(B)&(~C)&(D);
assign x6=(X)&(~Y)&(Z);
assign x7=(~X)&(~Y)&(Z);
assign x8=(~W)&(X)&(Y);
assign x9=(W)&(~X)&(Y);
assign x10=(W)&(X)&(Y);
assign F1=x1|x2|x3|x4|x5;
assign F2=x6|x7|x8|x9|x10;
endmodule
```
**RTL realization**
![image](https://github.com/user-attachments/assets/1fb80903-c01f-4614-a8a7-cd5f8e14b628)

**Output:**
![image](https://github.com/user-attachments/assets/3691efe1-161e-4581-9cb3-a62d926fb20a)

**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

