# 🛡️ YOLO Intruder Alert System

[![Python](https://img.shields.io/badge/Python-3.10-blue?logo=python)](https://www.python.org/)
[![YOLO](https://img.shields.io/badge/YOLOv5-Object%20Detection-red?logo=pytorch)](https://github.com/ultralytics/yolov5)
[![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-Edge%20Processing-A22846?logo=raspberrypi)](https://www.raspberrypi.org/)
[![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-5C3EE8?logo=opencv)](https://opencv.org/)
[![Status](https://img.shields.io/badge/Status-Prototype-orange)]()

---

## 📖 Overview

The **YOLO Intruder Alert System** is a **real-time computer vision-based security system** designed to detect unauthorized people in restricted areas using **YOLO (You Only Look Once)** object detection. It runs on **Raspberry Pi** for edge processing and can trigger alerts via email or other notification systems.

---

## 🎯 Key Features

-   **Real-time Intruder Detection** using YOLOv5
-   **Lightweight Deployment** optimized for Raspberry Pi
-   **Instant Notifications** (currently email, expandable to Blynk/MQTT)
-   **Image Capture & Storage** for evidence
-   **Customizable Detection Zones** (optional for fine-tuned monitoring)

---

## 🧰 Tech Stack

-   **Hardware:** Raspberry Pi 4, Camera Module (USB or Pi Camera)
-   **Programming:** Python
-   **Libraries:**
    -   `OpenCV` – Image processing & camera handling
    -   `YOLOv5` – Pretrained object detection (requires `ultralytics` package for YOLOv5)
    -   `smtplib` – Email notifications
-   **Optional:** Blynk or MQTT for IoT-based remote alerts (future integration)

---

## 🗂 Project Structure

```

YOLO-Intruder-Alert/
│
├── models/                 \# YOLO models (e.g., yolov5s.pt)
├── alert\_images/           \# Captured intruder images
├── main.py                 \# Main detection & alert script
├── packages.txt            \# Required Python packages
├── config.py               \# Configuration (email, thresholds, etc.)
└── README.md

````

---

## ⚙️ Installation & Setup

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/xaatim/YOLO-Intruder-Alert.git](https://github.com/xaatim/YOLO-Intruder-Alert.git)
    cd YOLO-Intruder-Alert
    ```

2.  **Install Python dependencies**
    ```bash
    pip install -r packages.txt
    ```

3.  **Download YOLO weights**
    Place your YOLOv5 weights (e.g., `yolov5s.pt` or custom trained weights) inside the `models/` folder. You can download `yolov5s.pt` from the [Ultralytics YOLOv5 repository](https://github.com/ultralytics/yolov5/releases).

4.  **Configure email alerts (optional but recommended)**
    Edit `config.py` with your SMTP server details, sender email, recipient email, and password for email notifications.

5.  **Run the system**
    ```bash
    python main.py
    ```

---

## 📷 Visuals

### Detection in Action:

Images of detected intruders are automatically stored in the `alert_images/` directory.


-----

## 🚀 Future Improvements

  * Add **Zone-based Detection** (monitor only specific areas in frame).
  * Integrate **Cloud Storage** for captured images (e.g., Google Drive, AWS S3).
  * Implement **Face Recognition** for authorized personnel filtering.
  * Build a **Web Dashboard** for live feed & alerts.
  * Expand notification methods to include **Blynk** or **MQTT** for IoT-based remote alerts.

-----

## 📄 License

This project is licensed under the **MIT License**. See [`LICENSE`](https://www.google.com/search?q=./LICENSE) for details.

-----

## 👤 Author

**Hatim Ahmed Hassan** – 2025

For inquiries or collaborations: **[xayari229@gmail.com](mailto:xayari229@gmail.com)**
