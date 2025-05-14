# 🎛️ Gesture Volume Control with OpenCV & MediaPipe

Control your system volume in real time using your fingers and a webcam.  
Built with Python, OpenCV, MediaPipe, and Pycaw.

---

## 📸 Demo

GIF will be added later for reference.
![image](https://github.com/user-attachments/assets/43c58d41-2fd4-4bf9-ba45-7ac6a9d8d88d)


---

## 🚀 Features

- ✋ Detects hand and landmarks in real time using MediaPipe
- 👉 Tracks thumb and index fingertips
- 📏 Calculates distance between fingers to determine gesture
- 🔊 Maps gesture distance to system volume using Pycaw
- 📊 Displays:
  - Dynamic volume bar
  - Volume percentage
  - FPS counter

---

## ⚙️ How It Works

1. Use OpenCV to capture webcam input
2. [MediaPipe](https://github.com/google-ai-edge/mediapipe/blob/master/docs/solutions/hands.md) detects hand and landmarks
3. Track landmark `4` (thumb tip) and `8` (index tip)
4. Calculate Euclidean distance between points
5. Use `np.interp()` to map distance to dB volume range
6. Set system volume with [pycaw](https://github.com/AndreMiras/pycaw)
7. Render visual feedback: circles, lines, volume bar, and percentage

---

## 🧩 Dependencies

```bash
pip install opencv-python mediapipe comtypes pycaw numpy
```

## 🛠️ Run
```bash
python VolumeHandControl.py
```

## 📁 File Structure
```plaintext
📦 opencv-sandbox
 ┣ 📜 VolumeHandControl.py         # Main script
 ┣ 📜 HandTrackingModule.py        # MediaPipe hand detector class
 ┗ 📜 README.md
```
