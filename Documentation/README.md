# 📘 Documentation

This folder contains all technical documentation, design files, and supporting materials for the **PLC SQO Motors & Pilot Lights Control System** project.

---

### 📑 Contents

| File                        | Description |
|-----------------------------|-----------|
| Ladder_Program.pdf          | Full ladder logic diagram (LAD 2) with SQO, TON timer, and reset logic |
| Binary_Table_Steps.pdf      | Detailed truth table and B3:0 binary file configuration for all 4 steps |
| SQO_Logic_Diagram.pdf       | Visual representation of the sequencer states and output mapping |
| Project_Report.pdf          | (Optional) Full project report including analysis and testing results |
| Sequence_Steps_Explanation.md | Text description of each step in the sequence |

---

### 🎯 Project Summary

**Title:** PLC SQO Motors & Pilot Lights Control System  
**Platform:** LogixPro Simulator (RSLogix 500)  
**Main Instruction:** Sequencer Output (`SQO`)  
**Control Elements:**  
- Two Motors (O:2/0, O:2/1)  
- Three Pilot Lights (Green, Red, Yellow)  

---

### 🔧 Key Technical Details

- **Sequencer File**: `B3:0` (Length = 4 steps)
- **Mask**: `FFFFh` (Full 16-bit pass)
- **Destination**: `O:2` (Output module)
- **Control Register**: `R6:0`
- **Operating Modes**:
  1. Manual step advancement using Start Push Button (`I:1/0`)
  2. Automatic cycling using TON Timer (`T4:0`)
- **Reset**: Push Button (`I:1/1`) → `RES R6:0`

---

### Academic Origin

This project is based on the **PLC Sequencer Logic** course on LinkedIn Learning.  
**Instructor / Author**: LinkedIn Learning  
**Reference**: [PLC Sequencer Logic](https://www.linkedin.com/learning/plc-sequencer-logic/)

The core exercise (motors + pilot lights sequencing using SQO) follows the instructor’s example, while the implementation, dual-mode operation (manual + automatic), and full documentation were developed independently.

---

### Scope of Work

- Complete ladder logic implementation in LogixPro
- Proper configuration of the binary table (`B3` file)
- Masking strategy explanation
- Addition of TON timer for automatic operation
- Reset functionality at any point in the sequence
- Comprehensive visual and textual documentation

---

**Made with determination ❤️**

---

**Note:**  
All materials in this folder are for educational purposes. Real-world applications must incorporate proper safety interlocks, motor acceleration/deceleration timing, and emergency stop circuits.
