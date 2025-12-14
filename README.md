# Advanced-Encryption-Standard-128-bit
##  Project Overview

This repository contains the **Register-Transfer Level (RTL) design** and implementation of a high-speed, fully synthesized **Advanced Encryption Standard (AES-128)** cryptographic core. The design is optimized for high-throughput, low-latency data encryption and decryption, targeting deployment on an FPGA platform.

The core architecture includes a dedicated **Finite State Machine (FSM)** for control and an integrated **UART bridge** for real-time communication, demonstrating a complete system-on-chip (SoC) style solution.

##  Key Features & Technical Achievements

  * **Verilog HDL Implementation:** Full RTL design of the AES-128 cipher (encryption and decryption) compliant with the **NIST FIPS 197 Standard**.
  * **Hardware Integration:** Fully synthesized and implemented on the **Xilinx Artix-7 FPGA (Basys 3)**, demonstrating practical deployment capability.
  * **Real-Time Communication:** Integrated a **UART bridge** to enable real-time plaintext/ciphertext transfer and control with a Host PC, validating the system in a real-world communication context.
  * **Optimized Control:** Utilized a dedicated **Finite State Machine (FSM)** to manage the 10 rounds of transformation, key expansion scheduling, and the UART interface protocol.
  * **Timing Closure & Robustness:** Achieved successful **Timing Closure** and reduced logic congestion across the target FPGA architecture through targeted clock management and pipeline optimization.
  * **External Verification Script:** Developed a complementary **Python-based script** on the Host PC to automate test vector generation and verify the FPGA output against software-based AES calculation, ensuring transactional integrity.

##  Design Architecture

The design follows a modular, synthesizable structure:

1.  **AES Core:** Implements the four core transformations ($\text{SubBytes}$, $\text{ShiftRows}$, $\text{MixColumns}$, $\text{AddRoundKey}$) and their inverses.
2.  **Key Expansion Unit:** Generates the 11 round keys from the 128-bit input key.
3.  **Top-Level FSM:** Controls the sequencing of the 10 AES rounds and handles external control signals.
4.  **UART Bridge:** Handles serial-to-parallel conversion for data input/output with the PC interface.

##  Tools and Technologies

  * **Hardware Description Language (HDL):** Verilog
  * **EDA Toolchain:** Xilinx Vivado (Synthesis, Implementation, Bitstream Generation)
  * **Simulation & Verification:** ModelSim / Vivado Simulator
  * **Target Hardware:** Digilent Basys 3 Development Board (Xilinx Artix-7 FPGA)
  * **Host Software:** Python (Verification Script)



