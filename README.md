# hardware-accelerated-CNN-inference-on-ZCU104-using-Vitis-AI
# Tiny YOLOv3 on ZCU104 using Vitis AI DPU

## Overview
This project demonstrates hardware-accelerated object detection using Tiny YOLOv3 on the Xilinx ZCU104 FPGA board with Vitis AI.

The inference runs on the DPU (DPUCZDX8G), not on CPU.

## Hardware
- Xilinx ZCU104
- Ethernet (SSH access)
- USB-UART
- SD card (Vitis AI image)

## Software
- Vitis AI 3.0
- DPUCZDX8G
- Tiny YOLOv3 INT8 model

## DPU Verification
```bash
xdputil query
