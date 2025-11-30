# 🔐 Hardware Authentication System with Alarm Mechanism

**Authors:** P. Sathvik Kumar  
**Software Used:** Xilinx Vivado  
**HDL:** Verilog  
**College:** CVR College Of Engineering

---

## 📌 Project Overview

This project implements a **Hardware-Based Authentication System** using **Verilog HDL**.  
Unlike software authentication, this system is implemented directly in hardware logic, making it **secure, fast, and resistant to common software attacks**.

The system validates a **4-digit password**.  
If the password is incorrect for **three consecutive attempts**, the system activates an **alarm**.

---

## 🧠 Functional Description

The system follows **three operational phases**, controlled by an FSM inside an `always` block.

### 🔁 1. Reset Phase
- Triggered when `rst_n = 0`
- Clears:
  - `entered_pwd`
  - `digit_count`
  - `wrong_attempts`
- Deactivates:
  - `unlock`
  - `alarm`
- Ensures a secure system startup.

### 🔢 2. Password Entry Phase
- Active when `enter = 0`
- On every clock cycle:
  - The system reads `key_in`
  - Concatenates the digit into `entered_pwd`
  - Increments `digit_count` until 4 digits are entered

### ✔️ 3. Verification Phase
Triggered when `enter = 1`

- Compares `entered_pwd` with `CORRECT_PWD`
- **If correct:**  
  - `unlock = 1`  
  - `wrong_attempts` reset to 0  

- **If incorrect:**  
  - `unlock = 0`  
  - `wrong_attempts++`  
  - If `wrong_attempts == 3`, then `alarm = 1`

---

## 🏁 Conclusion

The **Hardware Authentication System** successfully demonstrates a secure and robust access-control mechanism implemented entirely using **digital hardware logic**.  
By embedding the authentication logic into the circuit, the system becomes significantly more resistant to tampering and common software vulnerabilities.

This project deepens understanding of FSM design, hardware security mechanisms, and real-time digital verification processes.

---

## 📂 Future Enhancements
- Adding keypad debounce logic  
- Supporting multi-user passwords  
- Integrating LCD/OLED display  
- Implementing biometric-based authentication  

---

## 🚀 How to Run
1. Open Xilinx Vivado  
2. Create a new RTL project  
3. Add Verilog source code & testbench  
4. Run:
   - Behavioral Simulation  
   - Synthesis  
   - Implementation  
5. Generate Bitstream (optional)  
6. View power/timing reports  

---
