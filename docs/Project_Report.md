# Project Report  
## CNN Accelerator on ZCU104

---

## 1. Introduction

Convolutional Neural Networks (CNNs) are widely used in computer vision applications such as object detection, image classification, and autonomous systems.

This project focuses on accelerating CNN inference using FPGA fabric while ARM handles control and preprocessing.

---

## 2. Problem Statement

Implement an AI-based object detection system using ARM + FPGA architecture with CNN running in hardware.

---

## 3. Methodology

1. Dataset preprocessing
2. CNN model selection (Tiny-YOLO / MobileNet)
3. Quantization for FPGA deployment
4. Hardware accelerator design in Verilog
5. Integration using AXI-Stream
6. Software control using Vitis

---

## 4. Hardware Architecture

- ARM PS handles:
  - Image resize
  - Normalization
  - Control

- FPGA PL handles:
  - Convolution
  - Feature extraction
  - Inference

---

## 5. Results

- Hardware acceleration achieved
- Reduced latency compared to software-only execution
- Efficient ARM + PL communication

---

## 6. Conclusion

The project successfully demonstrates CNN acceleration using FPGA in a heterogeneous ARM + PL architecture.
