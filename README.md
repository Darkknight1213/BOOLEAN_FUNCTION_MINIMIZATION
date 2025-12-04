# Boolean Function Minimization

### **AIM**
To implement the given logic functions and verify their operation in **Quartus II** using **Verilog programming**.

---

### **Given Logic Functions**

- **F1 = A’B’C’D’ + AC’D’ + B’CD’ + A’BCD + BC’D**  
- **F2 = xy’z + x’y’z + w’xy + wx’y + wxy**

---

### **Equipment Required**
- **Hardware:** PC, Cyclone II FPGA, USB Blaster  
- **Software:** Quartus Prime

---

### **Theory**
Boolean function minimization is the process of simplifying complex logical expressions without altering their output behavior. The minimized form reduces the number of logic gates used, optimizing circuit design and improving efficiency.  

The given Boolean functions are implemented using basic logic operations such as **AND**, **OR**, and **NOT** gates, and then combined to form their respective outputs, **F1** and **F2**.

---

### **Procedure**
1. Type the program in **Quartus Prime** software.  
2. Compile and run the program.  
3. Generate the **RTL schematic** and save the logic diagram.  
4. Create nodes for input and output signals.  
5. Generate the **timing diagram** for various input combinations and verify the results.

---

### **Verilog Program**
```
/* Program to implement the given logic function and verify its operations in Quartus using Verilog programming. */
module Boolean_min(A, B, C, D, W, X, Y, Z, F1, F2);
input A, B, C, D, W, X, Y, Z;
wire x1, x2, x3, x4, x5, x6, x7, x8, x9, x10;
output F1, F2;

assign x1 = (~A) & (~B) & (~C) & (~D);
assign x2 = (A) & (~C) & (~D);
assign x3 = (~B) & (C) & (~D);
assign x4 = (~A) & (B) & (C) & (D);
assign x5 = (B) & (~C) & (D);

assign x6 = (X) & (~Y) & (Z);
assign x7 = (~X) & (~Y) & (Z);
assign x8 = (~W) & (X) & (Y);
assign x9 = (W) & (~X) & (Y);
assign x10 = (W) & (X) & (Y);

assign F1 = x1 | x2 | x3 | x4 | x5;
assign F2 = x6 | x7 | x8 | x9 | x10;
endmodule

// Developed by: Mohamed Riyaz Ahamed
// Register Number: 212224240092
```

---

### **Truth Table**
![Truth Table F1](https://github.com/user-attachments/assets/7e5956fd-2a45-42b5-97ef-90e508d80ae4)  
![Truth Table F2](https://github.com/user-attachments/assets/ab1199f6-937a-4a51-939e-0b2dbefdc640)

---

### **RTL Realization**
![RTL Realization](https://github.com/user-attachments/assets/ef46292a-9514-4ff6-b609-15292b2421f3)

---

### **RTL Schematic**
![RTL Schematic](https://github.com/user-attachments/assets/bd68aca9-646d-49a7-8e3e-9e80922fa85d)

---

### **Result**
Thus, the given Boolean functions **F1** and **F2** were successfully implemented and their operations verified using **Verilog programming** in **Quartus II**.

---
