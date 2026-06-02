# Hi there, I'm Le Chanh Nguyen (Arilla26) 👋

<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&color=36BCF7&center=true&vCenter=true&width=500&lines=Computer+Engineering+Senior+%40+HCMUT;RTL+Design+%26+FPGA+Engineer;Zynq-7020+%2F+Vivado+%2F+SystemVerilog;Microarchitecture+%26+Timing+Closure" alt="Typing SVG" />
</div>

<p align="center">
  <a href="https://linkedin.com/in/le-chanh-nguyen-1a1159309"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:nguyen.learilla26@hcmut.edu.vn"><img src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
</p>

---

## 🚀 About Me

I am a final-year **Computer Engineering** student at **Ho Chi Minh City University of Technology (HCMUT)** with a strong interest in **digital logic design**, **microarchitecture exploration**, and **hardware acceleration for AI workloads**.

My current focus is bridging algorithms and silicon flow on **Xilinx Zynq-7020** SoC platforms, using **SystemVerilog**, **AXI4** interconnect, and **post-route timing analysis**.

- 🔭 Currently working on **KV Cache Management for Long-Context LLM Inference** on **Zynq-7020 (Arty Z7-20)** — capstone project closing timing at WNS = +1.736 ns at 50 MHz.
- 🌱 Exploring **computer architecture (RISC-V)**, **AXI4-Lite/Full protocols**, **cache replacement policies (Tree-PLRU, FIFO, LFSR)**, and **BF16 numerical encoding**.
- ⚡ Fun fact: I enjoy chasing fan-out bottlenecks through `report_timing` more than I probably should.

---

## 🛠️ Tech Stack

| **Category** | **Technologies** |
| :--- | :--- |
| **HDL** | ![Verilog](https://img.shields.io/badge/Verilog-B02030?style=flat-square) ![SystemVerilog](https://img.shields.io/badge/SystemVerilog-181717?style=flat-square) |
| **Software** | ![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white) ![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat-square&logo=c%2B%2B&logoColor=white) ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![Bash](https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnu-bash&logoColor=white) |
| **FPGA / Hardware** | ![Vivado](https://img.shields.io/badge/Xilinx-Vivado-red?style=flat-square) ![Zynq-7020](https://img.shields.io/badge/Zynq--7020-Arty%20Z7-blue?style=flat-square) ![RISC-V](https://img.shields.io/badge/RISC--V-Arch-black?style=flat-square) |
| **Tools** | ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black) ![XSim](https://img.shields.io/badge/Xilinx-XSim-red?style=flat-square) ![LaTeX](https://img.shields.io/badge/LaTeX-008080?style=flat-square&logo=latex&logoColor=white) |

---

## 🏆 Featured Projects

### 🚀 [KV Cache Manager for LLM Inference on FPGA](https://github.com/Arilla26/KV-Cache-Controller-for-LLM) `(Ongoing — Capstone)`

> **Zynq-7020 · SystemVerilog · AXI4 · BF16**
> * Hardware-managed KV cache for Qwen2.5-0.5B LLM inference (SnapKV sparse attention workload).
> * **1,641 lines** of SystemVerilog across 7 modules: 11-state controller FSM, 512-set × 8-way associative cache.
> * Replacement: **Tree-PLRU** (*N*−1 bits/set) with FIFO and LFSR alternatives, Fibonacci-hash address mapping.
> * On-the-fly **BF16 truncation codec** achieving 2:1 compression with bounded error ε ≤ 2⁻⁷.
> * **AXI4-Lite slave** (control) + **AXI4-Full master via S_AXI_HP0** (data plane to DDR3, bypassing ARM CPU).
> * Timing closure: **WNS = +1.736 ns @ 50 MHz**, 16 logic levels, 25,342 LUT (47.6%), 20 BRAM tiles.
> * Hit rate: **90.79%** on medium trace (256-token prefill) across 9 cache configurations.

### 💻 [Single-Cycle RISC-V Processor (RV32I subset)](https://github.com/Arilla26/Single-Cycle-RISC-V-Processor)

> **Verilog · Xilinx XSim · Icarus Verilog**
> * Single-cycle processor implementing an **RV32I subset** (ADD/SUB/AND/OR/SLT, ADDI, LW/SW, BEQ).
> * **5 functional modules** (IF/ID/EX/MEM/WB) integrated through `cpu_top` — *no pipeline registers*, one instruction per clock cycle.
> * 32×32-bit register file with hardwired `x0=0`, 256×32-bit instruction/data memories.
> * Control unit uses **default-then-override** signal assignment to avoid inferred latches.
> * Two self-checking testbenches: arithmetic/memory flow via `instr.mem`, and BEQ TAKEN/NOT-TAKEN coverage with custom RV32I encoders.

### ⏱️ [Multifunctional Sports Stopwatch on FPGA](https://github.com/Arilla26/Digital-Sports-Watch)

> **Verilog · Arty Z7 · LCD/7-Segment**
> * Digital stopwatch with **10 ms precision** (`hh:mm:ss.xx` format), featuring pause/resume, manual time adjustment, and lap-time saving.
> * **6 hierarchical modules**: clock divider (1 Hz / 2 Hz / 5 Hz / 1 kHz), time counter with blink mode, button debouncer, Hex-to-BCD converter, 12-digit 7-segment decoder, FSM-based LCD transfer controller.
> * Custom **20×4 LCD driver** handling initialization sequences and data packing via parallel interface.

---

<div align="center">
  <i>"The synthesis report says 'met' — but is it really?"</i>
</div>
