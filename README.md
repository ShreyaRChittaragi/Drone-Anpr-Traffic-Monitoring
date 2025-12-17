# Drone-Based Traffic Video Analysis (ANPR)

---

## Overview
This project implements a traffic video analysis pipeline focused on
Automated Number Plate Recognition (ANPR). It processes traffic or drone
footage to detect license plates using YOLO and extract plate numbers
using OCR.

The system demonstrates the following architecture:

DRONE → KINESIS → YOLO → OCR → DYNAMODB → DASHBOARD

Cloud components are mocked to explain data flow and system design.

---

## Features
- YOLO-based license plate detection (.pt model support)
- OCR extraction using EasyOCR / Tesseract
- Frame skipping for efficient processing
- Bounding box visualization on video frames
- Confidence scoring and timestamped detections
- Mock AWS Kinesis Video Streams integration
- Mock AWS DynamoDB storage flow

---

## Tech Stack
- Python
- OpenCV
- Ultralytics YOLO (YOLOv5 / YOLOv8)
- EasyOCR / Tesseract
- NumPy
- Matplotlib

---

## Project Structure
drone-anpr-traffic-monitoring/
├── notebooks/ # Main notebook
├── data/ # Input videos
├── models/ # YOLO .pt models
├── outputs/ # Annotated frames / logs
├── src/ # Future modularization
└── README.md

---

## How It Works
1. Upload a traffic or drone video
2. Video is decoded into frames
3. YOLO detects license plates
4. Detected regions are cropped
5. OCR extracts plate text
6. Results are logged with confidence and timestamps
7. Output frames are visualized

---

## Use Cases
- Traffic monitoring
- ANPR system demonstration
- Smart city research
- Computer vision portfolios

---

## Notes
- AWS components are mocked
- Focus is on pipeline design and system flow
- Intended for educational and portfolio use

---

## License
MIT License
