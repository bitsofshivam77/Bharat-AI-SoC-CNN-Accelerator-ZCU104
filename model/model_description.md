# CNN Model Description

## Model Selected

A lightweight Convolutional Neural Network (CNN) architecture inspired by Tiny-YOLO / MobileNet is considered for hardware acceleration on FPGA.

---

## Why This Model?

The model was selected because:

- Lightweight architecture suitable for FPGA
- Lower computational complexity
- Efficient for real-time object detection
- Suitable for embedded systems like PYNQ-Z2

---

## Input Specifications

- Input Size: 224 x 224 RGB Image
- Input Format: 8-bit quantized data
- Preprocessing:
  - Resize
  - Normalization
  - Pixel scaling

---

## Model Architecture (Simplified)

The CNN consists of:

1. Convolution Layers
2. ReLU Activation
3. Pooling Layers
4. Fully Connected / Detection Head

Only convolution operations are hardware accelerated on FPGA.

---

## FPGA Acceleration Strategy

- Convolution operations mapped to FPGA Programmable Logic (PL)
- AXI-Stream used for PS-PL communication
- ARM Cortex-A9 handles:
  - Image preprocessing
  - Control logic
  - Post-processing
  - Bounding box generation

---

## Quantization

To enable efficient FPGA implementation:

- Model weights quantized to 8-bit
- Fixed-point arithmetic used in hardware
- Reduced memory bandwidth requirement

---

## Deployment Platform

- Board: PYNQ-Z2
- SoC: Xilinx Zynq-7000
- ARM: Dual-core Cortex-A9
- FPGA fabric used for CNN acceleration

---

## Key Innovation

Instead of running the CNN fully on ARM processor, the computationally intensive convolution layers are offloaded to FPGA fabric, significantly improving performance and reducing latency.
