# Hand Gesture Mouse Controller 🤖👆

A computer vision-based mouse controller using hand gestures, powered by MediaPipe and PyAutoGUI.

## Features ✨
- Move cursor using fingers
- Left/Right click detection
- Double click gesture
- Screenshot capture
- Real-time hand tracking visualization

## Prerequisites 📋
- Python 3.7+
- Webcam
- [Required Libraries](#dependencies)

## Installation ⚙️

1. Clone repository:
```bash
git clone https://github.com/yourusername/hand-gesture-mouse.git
cd hand-gesture-mouse
```

2. Create virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # Linux/MacOS
venv\Scripts\activate  # Windows
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## Dependencies 📦
- OpenCV (`opencv-python`)
- MediaPipe (`mediapipe`)
- PyAutoGUI (`pyautogui`)
- NumPy (`numpy`)
- pynput (`pynput`)

## Usage 🖱️
Run the main script:
```bash
python main.py
```

**Control Scheme:**
- 👆 **Move Cursor**: Extended index and middle finger joined with thumb closed
- 🤏 **Left Click**: Index finger extended + thumb bent
- 🖖 **Right Click**: Middle finger extended + thumb bent
- ✌️ **Double Click**: Both index and middle fingers bent
- 🤘 **Screenshot**: Index/middle fingers bent + thumb close (Open five fingers then do a press like gesture)
- **Stop at a Point**: Thumb, index and middle finger extended while others are bent

Press `Q` to quit the application.

## Gesture Detection Logic 🔍
Key detection logic can be found in:
```python:main.py
startLine: 69
endLine: 92
```

Angle/distance calculations are handled by:
```python:util.py
startLine: 3
endLine: 14
```
**Note:** This project uses a simple gesture detection approach. For more complex gestures, consider using machine learning models or more sophisticated gesture recognition techniques.

## Troubleshooting 🛠️
**Webcam Not Detected:**
- Ensure camera is not being used by other applications
- Verify camera permissions

**Gesture Detection Issues:**
- Maintain good lighting conditions
- Keep hand within camera frame
- Avoid rapid movements

## Contributing 🤝
Contributions welcome! Please follow standard GitHub workflow:
1. Fork repository
2. Create feature branch
3. Submit Pull Request