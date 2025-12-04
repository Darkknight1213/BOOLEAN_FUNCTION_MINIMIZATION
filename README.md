# BOOLEAN_FUNCTION_MINIMIZATION

**AIM:**

To implement the given logic function verify its operation in Quartus using Verilog programming.

F1= A’B’C’D’+AC’D’+B’CD’+A’BCD+BC’D 

F2=xy’z+x’y’z+w’xy+wx’y+wxy

**Equipment Required:**

Hardware – PCs, Cyclone II , USB flasher

**Software – Quartus prime**

**Theory**

**Logic Diagram**

**Procedure**
```
1.	Type the program in Quartus software.

2.	Compile and run the program.

3.	Generate the RTL schematic and save the logic diagram.

4.	Create nodes for inputs and outputs to generate the timing diagram.

5.	For different input combinations generate the timing diagram.

```
**Program:**
```
/* Program to implement the given logic function and to verify its operations in quartus using Verilog programming. 
module Boolean_min(A,B,C,D,W,X,Y,Z,F1,F2);
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
 Developed by: Mohamed Riyaz Ahamed
 RegisterNumber: 212224240092
*/
```
**TRUTH TABLE**
![Screenshot 2024-11-26 134353](https://github.com/user-attachments/assets/7e5956fd-2a45-42b5-97ef-90e508d80ae4)
![Screenshot 2024-11-26 134419](https://github.com/user-attachments/assets/ab1199f6-937a-4a51-939e-0b2dbefdc640)


**RTL realization**
![Screenshot 2024-11-26 133954](https://github.com/user-attachments/assets/ef46292a-9514-4ff6-b609-15292b2421f3)



**RTL**
![Screenshot 2024-11-26 134128](https://github.com/user-attachments/assets/bd68aca9-646d-49a7-8e3e-9e80922fa85d)



**Result:**

Thus the given logic functions are implemented using and their operations are verified using Verilog programming.

