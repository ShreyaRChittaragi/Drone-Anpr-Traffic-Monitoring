Drone-Based Traffic Video Analysis (ANPR)
Overview

This project implements a traffic video analysis pipeline focused on Automatic Number Plate Recognition (ANPR).
It processes traffic or drone footage to detect license plates using YOLO, extract text using OCR, and demonstrate how such data can flow through a real-time cloud-style architecture.

The design follows this pipeline:

DRONE → KINESIS → YOLO → OCR → DYNAMODB → DASHBOARD

Cloud services are mocked to explain the architecture and data flow.

What This Project Does

Reads traffic / drone video footage

Detects license plates using a YOLO model

Crops detected plate regions

Extracts plate text using OCR

Attaches confidence scores and timestamps

Demonstrates how detections can be streamed and stored

Key Features

YOLO-based license plate detection (.pt support)

OCR using EasyOCR / Tesseract

Frame skipping for efficient processing

Bounding box visualization on frames

Timestamped and confidence-based results

Mock integration of AWS Kinesis and DynamoDB

Tech Stack

Python

OpenCV

Ultralytics YOLO (YOLOv5 / YOLOv8)

EasyOCR / Tesseract

NumPy

Matplotlib

Project Structure
drone-anpr-traffic-monitoring/
├── notebooks/        # Main notebook
├── data/             # Input videos
├── models/           # YOLO .pt models
├── outputs/          # Annotated frames / logs
├── src/              # Future modularization
└── README.md

How It Works

Upload a traffic or drone video

Video is processed frame by frame

YOLO detects license plates

OCR extracts text from detected plates

Results are logged with confidence and timestamps

Output frames are visualized

Use Cases

Traffic monitoring and analysis

ANPR system demonstration

Smart city and surveillance research

Computer vision system design portfolios

Notes

Cloud components (Kinesis, DynamoDB) are mocked

The focus is on pipeline design and system flow

Intended for learning, demonstration, and portfolio use

License

MIT License
