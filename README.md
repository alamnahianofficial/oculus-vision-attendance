# Oculus — Smart Vision Attendance & Security System

<p align="center">
  <img src="Assets/01-dashboard.png" alt="Dashboard Preview">
</p>

Oculus is an advanced computer vision platform designed for seamless attendance tracking and facility security. By utilizing real-time camera feeds, it provides automated facial recognition, personnel tracking, and instant security alerts without the need for physical badges or biometric scanners.

## System Interface Gallery

### Dashboard & Analytics
<p align="center">
  <img src="Assets/08-analytics.png" alt="Analytics" width="49%">
  <img src="Assets/10-reports.png" alt="Reports" width="49%">
</p>

### Detection & Camera Management
<p align="center">
  <img src="Assets/03-camera-sections.png" alt="Camera Sections">
</p>
<p align="center">
  <img src="Assets/04-detection-log.png" alt="Detection Log" width="49%">
  <img src="Assets/13-cross-check.png" alt="Cross Check" width="49%">
</p>

### Security & Alert Systems
<p align="center">
  <img src="Assets/06-security-alert.png" alt="Security Alert" width="49%">
  <img src="Assets/11-watchdogs.png" alt="WatchDogs" width="49%">
</p>

### Employee Management
<p align="center">
  <img src="Assets/02-employee-section.png" alt="Employee Section" width="49%">
  <img src="Assets/09-shifts.png" alt="Shifts" width="49%">
</p>

<details>
<summary><b>View Additional Interfaces</b></summary>
<br>
<p align="center">
  <img src="Assets/05-alert.png" alt="Alert">
</p>
<p align="center">
  <img src="Assets/07-security-alert.png" alt="Security Alert 2">
</p>
<p align="center">
  <img src="Assets/12-admin-panel.png" alt="Admin Panel">
</p>
</details>

---

## Key Features

- **Real-Time Facial Recognition:** Identifies personnel instantly using optimized YOLOv11 and AdaFace models.
- **Automated Attendance:** Logs entry and exit times with precision, automatically calculating late arrivals, early departures, and overtime.
- **Proactive Security Alerts:** Notifies administrators regarding unauthorized intrusions, blacklisted individuals, masked faces, suspicious baggage, and irregular after-hours activity.
- **Anti-Spoofing Mechanisms:** Detects and blocks fraudulent authentication attempts using photographs or pre-recorded videos.
- **Low-Light Enhancement:** Dynamically adjusts underexposed video frames to ensure reliable detection during nighttime or in poorly lit environments.
- **Automated Camera Calibration:** Simplifies deployment by enabling new cameras to configure themselves based on a single reference frame.
- **Continuous Learning:** The recognition pipeline progressively refines its accuracy based on historical environmental data.
- **Historical Auditing:** Allows administrators to process archived footage through the AI pipeline to verify attendance records retrospectively.
- **Centralized Dashboard:** A comprehensive web interface for managing analytics, monitoring alerts, and reviewing personnel histories.
- **Multi-Branch Scalability:** Designed to operate across diverse geographical locations with distinct timezone configurations.

## Technical Stack

- **Computer Vision:** YOLOv11, ByteTrack, AdaFace, MediaPipe
- **Backend Infrastructure:** FastAPI (Python)
- **Frontend Architecture:** Next.js 15
- **Database Systems:** PostgreSQL paired with pgvector for efficient similarity search
- **Deployment & Orchestration:** Docker, Redis, Celery

## System Workflow

1. The system ingests a continuous video stream from integrated cameras.
2. The vision pipeline processes each frame to detect individuals and extract facial embeddings.
3. Extracted embeddings are cross-referenced with the enrolled personnel database.
4. The backend records attendance metrics or triggers appropriate security protocols based on the identification results.
5. All data is visualized in real-time on the centralized administrative dashboard.

## Core Advantages

- **Hardware Agnostic:** Compatible with standard IP cameras via RTSP, ONVIF, USB, and other standard protocols.
- **Flexible Compute:** Supports acceleration on NVIDIA, AMD, and Intel GPUs, with a fallback to CPU-only execution.
- **Granular Security:** Implements role-based access control (RBAC) to ensure sensitive data is only accessible to authorized personnel.
- **Robust Operation:** Engineered to perform reliably despite real-world constraints such as suboptimal lighting, legacy camera hardware, and network instability.

---

## Intellectual Property Notice

This repository serves exclusively as a portfolio demonstration. The underlying source code, configuration files, and proprietary logic remain strictly confidential and are not distributed as open-source software. Unauthorized reproduction, modification, or redistribution of any materials within this repository is strictly prohibited.

© All rights reserved.
