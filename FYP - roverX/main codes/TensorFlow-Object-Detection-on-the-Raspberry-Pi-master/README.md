
# 📦 TensorFlow Object Detection API on Raspberry Pi

> 🔄 **Updated: January 2025**  
> A step-by-step guide to set up real-time object detection using a Raspberry Pi, TensorFlow, and a PiCamera or USB webcam.

---

## 🧠 What You'll Learn

This guide helps you set up the **TensorFlow Object Detection API** on a Raspberry Pi (Model 3B or above). By the end, you’ll be able to:
- Run object detection in real-time using a camera
- Use pre-trained models like MobileNet
- Build your own use-cases like a Pet Detector

---

## 🛠️ Installation Steps

### 1. Update the Raspberry Pi
Open Terminal and run:
```bash
sudo apt-get update
sudo apt-get dist-upgrade
```

---

### 2. Install TensorFlow and Required Packages
```bash
pip3 install tensorflow
sudo apt-get install libatlas-base-dev
sudo pip3 install pillow lxml jupyter matplotlib cython
sudo apt-get install python3-tk
```

---

### 3. Install OpenCV
```bash
sudo apt-get install libjpeg-dev libtiff5-dev libjasper-dev libpng12-dev
sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
sudo apt-get install libxvidcore-dev libx264-dev qt4-dev-tools
sudo pip3 install opencv-python
```

---

### 4. Install Protobuf Compiler
```bash
sudo apt-get install protobuf-compiler
protoc --version  # should return version info
```

---

### 5. Setup TensorFlow Directory and PYTHONPATH
```bash
mkdir ~/tensorflow1 && cd ~/tensorflow1
git clone --depth 1 https://github.com/tensorflow/models.git
```

Edit your `.bashrc`:
```bash
nano ~/.bashrc
```

Add at the end:
```bash
export PYTHONPATH=$PYTHONPATH:/home/pi/tensorflow1/models/research:/home/pi/tensorflow1/models/research/slim
```

Save and exit, then apply changes:
```bash
source ~/.bashrc
```

Compile `.proto` files:
```bash
cd ~/tensorflow1/models/research
protoc object_detection/protos/*.proto --python_out=.
```

---

### 6. Download the Pre-trained Model
```bash
cd ~/tensorflow1/models/research/object_detection
wget http://download.tensorflow.org/models/object_detection/ssdlite_mobilenet_v2_coco_2018_05_09.tar.gz
tar -xzvf ssdlite_mobilenet_v2_coco_2018_05_09.tar.gz
```

---

### 7. Run Object Detection
Download the detection script:
```bash
wget Object_detection_picamera.py
```

Run:
```bash
python3 Object_detection_picamera.py          # For PiCamera
python3 Object_detection_picamera.py --usbcam # For USB webcam
```

---


### Description
Detect your pet near a door and send an alert using the Pet_detector.py script. Works with the same TensorFlow setup.

Download and run:
```bash
wget Pet_detector.py
python3 Pet_detector.py
```

To send alerts via SMS, configure the following environment variables:
```bash
export TWILIO_ACCOUNT_SID=your_sid
export TWILIO_AUTH_TOKEN=your_token
export MY_DIGITS=your_phone
export TWILIO_DIGITS=twilio_phone
```

Or comment out SMS lines in the script if not using Twilio.

---

## 🗂 Directory Structure
```
~/tensorflow1/models/research/object_detection/
│
├── Object_detection_picamera.py
├── Pet_detector.py
├── ssdlite_mobilenet_v2_coco_2018_05_09/
├── data/
│   └── label_map.pbtxt
```

---

## ❄️ Notes
- Use a heatsink on your Pi for extended sessions.
- You can swap models by changing model path in the script.

---

## 🙌 Created By
**Ammar Hanif**  
Department of Computer Science  
University of South Asia  
Final Year Project – 2025
