# Bharat AI-SoC Student Challenge  
## CNN Accelerator on PYNQ-Z2 (ARM + FPGA)

---

## Project Overview

The system is implemented on the PYNQ-Z2 board (Xilinx Zynq-7000 SoC), which integrates a dual-core ARM Cortex-A9 Processing System (PS) with FPGA Programmable Logic (PL).

The CNN inference is accelerated in FPGA fabric while ARM handles preprocessing and postprocessing.

---

## Final Architecture
![System Architecture](architecture.png)

Camera / Dataset  
↓  
ARM Processor (PS)  
- Image Resize  
- Normalization  
- Control Logic  

↓ AXI-Stream  

FPGA Fabric (PL)  
- Quantized CNN Accelerator  

↓ AXI-Stream  

ARM Processor (PS)  
- Post-processing  
- Bounding Boxes  
- Display / Save Output  

---

## Hardware Used

- PYNQ-Z2 (Xilinx Zynq-7000 SoC)
- Camera / Image Dataset
- Serial Console (optional)

### PYNQ-Z2 Board Specifications
- Xilinx Zynq-7000 (XC7Z020)
- Dual-core ARM Cortex-A9
- FPGA Fabric (Programmable Logic)
- DDR3 Memory
- HDMI / USB / Ethernet Support


---

## Software Used

- Vivado
- Vitis
- Verilog
- C++
- OpenCV
- Tiny-YOLO / MobileNet

---

## Key Innovation

- CNN Inference runs on FPGA (PL)
- ARM handles system-level control
- Hardware acceleration improves performance
- AXI-Stream communication between PS and PL

---

## Repository Structure

- /verilog → Hardware accelerator modules
- /vitis → Embedded software
- /python → Image preprocessing scripts
- /docs → Documentation
- /images → Architecture diagrams

---

## Performance Goal

- Reduced inference latency
- Efficient hardware utilization
- FPGA-based acceleration over CPU-only implementation
  
## 📄 Final Report

Download the complete project report here:
[Click to View Report](final_report/BharatAISoC_CNN_Accelerator_PYNQZ2_TeamSubmission.pdf)
---

## 📜 License

Academic Project – Bharat AI-SoC Challenge
