# 🚬 Smoking Detection Web Application (YOLO + Django)

A web-based application for detecting **smoking activities** in images and videos using **YOLOv5** (object detection) and **Django** (web framework).  
This project integrates computer vision with an interactive web interface, allowing users to upload images or use webcam streams for real-time smoking detection.

---

## 🧠 Key Features

- 🔍 **YOLOv5 Model Integration** — detects smoking activity accurately in images and live video.
- 💻 **Django Backend** — manages web interface, file uploads, and detection logic.
- 📸 **Image & Video Input** — upload images or stream from webcam.
- 📊 **Visualization** — highlights smoking regions in the frame.
- 📁 **Custom Dataset Support** — trained model (`weights.pt`) can be replaced with your own YOLO weights.

---

## 🧩 Tech Stack

| Layer | Technology Used |
|-------|-----------------|
| Backend | Django 4.2 (Python 3.10) |
| Computer Vision | PyTorch, YOLOv5 |
| Frontend | HTML, CSS, Bootstrap |
| Environment | Virtualenv / Conda |
| Visualization | OpenCV, Matplotlib |

---

## ⚙️ Installation Guide

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/jecxk/Group_project_smoking_detection.git
cd Group_project_smoking_detection

2️⃣ Create and Activate a Virtual Environment
python -m venv smokeenv
smokeenv\Scripts\activate

3️⃣ Install Dependencies
pip install --upgrade pip setuptools wheel
pip install -r requirements.txt


If labelImg or scikit-learn causes errors, install manually:

pip install labelImg scikit-learn

4️⃣ Install Ultralytics (YOLO)
pip install ultralytics

🧠 How to Run the Project
Run Migrations
python manage.py makemigrations
python manage.py migrate

Start the Django Development Server
python manage.py runserver


Once started, visit the app at:
👉 http://127.0.0.1:8000/

🖼️ Using the App

Open your browser and go to http://127.0.0.1:8000/.

Upload an image or video for smoking detection.

The model will run inference and display detection results directly on the web interface.

You can replace the pretrained model at:

yolov5/epochs_100/weights.pt

🧰 Troubleshooting
Problem	Possible Fix
ultralytics not found	pip install ultralytics
YOLOv5 repo error	Remove cache and retry:
rmdir /s /q %USERPROFILE%\.cache\torch\hub\ultralytics_yolov5_master
OpenCV cv2.error: (-215:Assertion failed)	Ensure your image path or webcam source is valid
Git push error	Use a Personal Access Token (PAT) instead of password
