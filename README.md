# 🧮 32-bit Parameterised ALU in Verilog

This project implements a **parameterised Arithmetic Logic Unit (ALU)** in Verilog, supporting multiple arithmetic, logical, shift, and comparison operations. The design is scalable and can be configured for different data widths.

---

## 🚀 Features

- ✔ Parameterised data width (default: 32-bit)
- ✔ Arithmetic operations: ADD, SUB
- ✔ Logical operations: AND, OR, XOR
- ✔ Shift operations: SLL, SRL, SRA
- ✔ Comparison operations: SLT (signed), SLTU (unsigned)
- ✔ Status flags:
  - Zero flag
  - Carry-out flag
  - Overflow flag
  - Sign flag
- ✔ Proper 2’s complement subtraction handling
- ✔ Fully verified using a testbench

---

## 🧠 Design Details

- Subtraction is implemented using **2’s complement**:
  - `A - B = A + (~B + 1)`
- Overflow detection:
  - ADD: same sign inputs, different sign output
  - SUB: different sign inputs, result sign differs from A
- Shift amount is derived from the lower 5 bits of operand B

---


