# Face Recognition Attendance System

This project is a Django-based web application for managing attendance using face recognition technology. It supports real-time face detection and recognition using a camera (USB or IP camera).

## Features

- User authentication (admin and staff)
- Real-time face detection and recognition
- Attendance marking and reporting
- Admin dashboard for managing users and attendance records

## Requirements

- Python 3.7+
- Django
- OpenCV (`opencv-python`)
- dlib
- numpy
- Other dependencies listed in `requirements.txt`

## Installation

1. **Clone the repository**
   ```sh
   git clone <repository-url>
   cd Project-Face-attandence-system-version-1.0
   ```

2. **Install dependencies**
   ```sh
   pip install -r requirements.txt
   ```

3. **Apply migrations**
   ```sh
   python manage.py makemigrations
   python manage.py migrate
   ```

4. **Create a superuser**
   ```sh
   python manage.py createsuperuser
   ```

5. **Run the development server**
   ```sh
   python manage.py runserver
   ```

6. **Access the application**
   - Open [http://127.0.0.1:8000/](http://127.0.0.1:8000/) in your browser.
   - Admin panel: [http://127.0.0.1:8000/admin/](http://127.0.0.1:8000/admin/)

## Camera Setup

- For a USB camera, no extra configuration is needed.
- For an IP camera, update the camera URL in your code or settings:
  ```python
  cap = cv2.VideoCapture("rtsp://username:password@camera_ip:port/stream_path")
  ```

## Troubleshooting

- **Failed to capture frame for camera:**  
  - Check camera URL, network connection, and authentication details.
  - Test the camera stream in VLC or a browser.

- **No such file or directory:**  
  - Make sure you are in the correct project directory and `manage.py` exists.

Developed by Muthu Kumaran T
