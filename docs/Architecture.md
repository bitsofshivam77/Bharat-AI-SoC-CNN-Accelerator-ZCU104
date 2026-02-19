# System Architecture

## Data Flow

Camera/Dataset  
↓  
ARM PS (Preprocessing)  
↓ AXI-Stream  
FPGA PL (CNN Accelerator)  
↓ AXI-Stream  
ARM PS (Postprocessing)

---

## Key Components

- AXI-Stream Interface
- CNN Accelerator (Quantized)
- ARM Software Control
