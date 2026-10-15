# CraftifAI PipeGen Track 1: Edge Vision Perception Pipeline

An optimized edge vision object detection pipeline built for the CraftifAI Physical AI Hackathon. This project utilizes a lightweight **YOLOv8n** model exported to ONNX format, designed for high-speed perception and TensorRT compilation on NVIDIA edge hardware.

## 🚀 Project Overview & Problem Statement
* **Track:** PipeGen (Perception)
* **Chosen Scenario:** Workplace Safety Sentinel / Retail Shelf Monitor (Object Detection & Analytics)[cite: 1]
* **Model Architecture:** YOLOv8n (Object Detection)
* **Precision Format:** FP16 / FP32 optimized for TensorRT engines

## 📂 Repository Structure
```text
├── yolov8n.onnx              # Exported perception model artifact
├── detection_output.json     # Actionable JSON output metadata feed[cite: 1]
└── README.md                 # Project documentation & pipeline specification

Pipeline Flow & StagesRequirement Analysis: Designed to capture real-time feeds from local video streams or cameras to detect objects/persons of interest.   Pipeline IR & Model: Leverages a custom-exported YOLOv8n ONNX graph (yolov8n.onnx) with dynamic execution shapes[cite: 3].Compiler & Optimization: Targets NVIDIA GPU / Jetson environments[cite: 1, 2] to compile into a low-latency TensorRT engine for maximum frame rates.Actionable Output: Processes bounding box coordinates, class labels, and confidence scores into a structured detection_output.json payload (or MQTT feed) that downstream applications can act on instantly[cite: 1, 2].
