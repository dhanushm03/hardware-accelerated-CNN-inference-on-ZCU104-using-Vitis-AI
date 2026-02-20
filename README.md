# Tiny YOLOv3 on ZCU104 using Vitis AI DPU

# 🚀 Hardware Accelerated CNN Inference on ZCU104 using Vitis AI

---

## 📌 Project Overview

This project demonstrates **hardware-accelerated object detection** using the **Tiny YOLOv3** deep learning model deployed on the **Xilinx ZCU104 FPGA** platform with **Vitis AI 3.0**.

Unlike CPU-based inference, this implementation executes the neural network on the **DPU (Deep Processing Unit - DPUCZDX8G)** synthesized in the programmable logic (PL) of the FPGA.  

---

## 🎯 Objectives

- Deploy a quantized Tiny YOLOv3 model on FPGA hardware  
- Utilize the DPU accelerator for inference instead of ARM CPU  
- Verify correct DPU configuration and runtime execution  
- Perform object detection on test input image  
---

## 🖥️ Hardware Setup

The following hardware components were used:

- **Xilinx ZCU104 FPGA Development Board**
- Ethernet connection (for SSH access)
- USB-UART (for serial communication)
- SD Card flashed with Vitis AI image
- Power Supply (12V DC Adapter)

---

## 💻 Software Stack

The software environment consists of:

- **Vitis AI 3.0**
- DPUCZDX8G Hardware Overlay
- Tiny YOLOv3 INT8 Quantized Model
- Linux (Petalinux-based Vitis AI Image)
- Xilinx Runtime (XRT)

---

## 🏗️ System Architecture

1. Tiny YOLOv3 model is quantized to INT8 format.
2. The compiled `.xmodel` is deployed to the ZCU104 board.
3. The DPU accelerator executes inference in programmable logic.
4. ARM processor handles pre-processing and post-processing.

This architecture separates control and acceleration for efficient edge AI inference.

---

## 🔍 DPU Verification

Before running inference, the DPU must be verified.

Run the following command:

```bash
xdputil query
```

Expected output should display:

- DPU architecture
- Number of cores
- B4096 configuration (or similar)
- Running frequency

If DPU information is shown, hardware acceleration is successfully enabled.

## ⚡ Key Features

- ✔ Hardware-accelerated inference on FPGA  
- ✔ DPU-based execution (Not CPU-based)  
- ✔ INT8 quantized model optimization  
- ✔ Verified DPU configuration  

---

## 📁 Project Structure

```
hardware-accelerated-CNN-inference/
│
├── README.md
├── images/
│   ├── board.jpeg
│   ├── dog.jpg
│   └── output.png
├── setup_steps
├── result
└── LICENSE
```

---

## 🚀 Conclusion

This project demonstrates successful deployment of a deep learning object detection model onto FPGA hardware using Vitis AI.  
By leveraging the DPU accelerator, inference performance is improved compared to CPU-based execution, showcasing the effectiveness of hardware acceleration for edge AI applications.

---

## 📜 License

Apache 2.0 License
