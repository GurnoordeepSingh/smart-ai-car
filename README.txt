================================================================================
                           SMART AI CAR PROJECT
================================================================================

PROJECT DESCRIPTION:
Smart AI Car is an advanced computer vision system designed for autonomous 
vehicle perception. It combines multiple AI models to detect lanes, identify 
vehicle damage, and process real-time video feeds for intelligent decision-making.

================================================================================
FEATURES:
================================================================================

1. LANE DETECTION
   - Real-time lane tracking using computer vision
   - Automatic lane boundary identification
   - Integrated into the main vision pipeline

2. DAMAGE DETECTION
   - AI-powered vehicle damage detection
   - Uses YOLOv8 nano model (6.5 MB pretrained model)
   - Identifies physical damage on vehicles

3. WEB DASHBOARD
   - Flask-based web interface
   - Real-time detection monitoring
   - MySQL database integration for data persistence
   - Historical detection logging

4. REAL-TIME VIDEO PROCESSING
   - Live camera feed capture and processing
   - Multi-model inference on video frames
   - Output visualization with bounding boxes and lane markings

================================================================================
TECHNOLOGY STACK:
================================================================================

Programming Language: Python
Web Framework: Flask
Computer Vision: OpenCV (cv2)
Object Detection: YOLOv8 (Ultralytics)
Database: MySQL
Object Detection Model: YOLOv8 Nano (6.5 MB)

================================================================================
PROJECT STRUCTURE:
================================================================================

smart-ai-car/
├── app.py              - Flask web application for dashboard
├── main.py             - Main computer vision pipeline
├── requirements.txt    - Python dependencies (needs to be populated)
├── yolov8n.pt          - YOLOv8 Nano pretrained model (6.5 MB)
├── src/                - Source code modules directory
│   ├── lane_detection.py      - Lane detection algorithm
│   └── damage_detection.py    - Damage detection module
├── templates/          - HTML templates for Flask web interface
│   └── index.html      - Dashboard UI
└── static/             - Static assets (CSS, JavaScript, images)

================================================================================
USAGE:
================================================================================

MAIN VISION PIPELINE:
   python main.py
   - Activates webcam/connected camera
   - Processes video frames in real-time
   - Applies lane detection and damage detection
   - Press 'q' to quit the application

WEB DASHBOARD:
   python app.py
   - Starts Flask server on http://localhost:5000
   - Displays historical detection data from MySQL database
   - Shows detection logs with timestamps

================================================================================
DATABASE CONFIGURATION:
================================================================================

MySQL Connection Details (in app.py):
   - Host: localhost
   - User: udbhavvj
   - Password: Udbhavvj2006
   - Database: smartcar

Expected "detections" table with columns:
   - detection_id, timestamp, object_type, confidence, coordinates

================================================================================
