# 🎮 Hand Gesture Controlled Game Automation using Python & MediaPipe

Control **Hill Climb Racing** (or similar keyboard-based games) with your **hand gestures** using real-time computer vision and automation!

This project leverages **MediaPipe** for hand tracking, **OpenCV** for video processing, and **PyDirectInput** for simulating key presses — turning your hand into a game controller!

---

# 🖐️ Features

- Real-time hand tracking via webcam.
- Detects number of fingers shown:
  - ✊ 0 fingers → Brake (`Right Arrow`)
  - 🖐️ 5 fingers → Accelerate (`Left Arrow`)
- Controls games using virtual keyboard input.
- Built for Hill Climb Racing but can be adapted to others.

---

# 🛠️ Technologies Used

- 🔍 [MediaPipe](https://google.github.io/mediapipe/) – Hand Landmark Detection
- 🎥 OpenCV – Webcam Input & Visualization
- 🧠 PyDirectInput – DirectInput-compatible keyboard control
- 🐍 Python

---

# 📦 Installation

Make sure you're using **Python 3.12** (MediaPipe may not support 3.12+).  
Then install required libraries:

```console
pip install opencv-python
pip install mediapipe
pip install pydirectinput
```


# 🚀 How to Run
Open the game (Hill Climb Racing or any game using arrow keys).

Run the Python script:

```console
py -3.12 main.py
```

Place your hand in front of the webcam:

🖐️ Five fingers = Gas 

✊ Fist (0 fingers) = Brake 

Press q to close the webcam.

# 📸 Demo

![Brake](<Screenshot 2025-06-17 165758.png>)

![Gas](<Screenshot 2025-06-17 165612.png>)

# 🧠 How It Works

* MediaPipe detects 21 hand landmarks.

* Finger states are inferred based on the relative position of landmarks.

* A finger count is derived from the landmarks.

* Based on the count:

* pydirectinput.keyDown('left') or keyDown('right') is called.

* Smooth control using natural gestures.

# 📁 Folder Structure

```bash
GameAutomation
├──Demo.mp4
├──hand_landmarks.png
├──main.py
├──README.md
├──Screenshot_2025-06-17_165612.png
└──Screenshot_2025-06-17_165758.png
```

# ✅ Requirements

Python 3.12 (or 3.9)

Webcam

Keyboard-controlled game (e.g., Hill Climb Racing for PC)

# 📄 License

This project is open-source under the MIT License.

# 🙌 Acknowledgements

Google MediaPipe for making hand tracking accessible.

PyDirectInput for reliable input simulation.

Inspired by games like Hill Climb Racing and the endless potential of automation!


