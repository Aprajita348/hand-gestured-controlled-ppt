# 🖐️ Hand Gesture Controlled Presentation

A real-time computer vision-based presentation controller that enables users to control presentation slides using **7 hand gestures** and **voice commands**, eliminating the need for traditional mouse-based navigation.

The system uses webcam-based hand landmark detection to provide slide navigation, pointer control, drawing/annotation, annotation removal, zoom control, and voice-based interaction.

---

## 🚀 Features

### 🖐️ Hand Gesture Control

The system supports **7 distinct hand gestures** for presentation control:

| Gesture                  | Action                |
| ------------------------ | --------------------- |
| 👍 Thumb Up              | Previous Slide        |
| 🤙 Pinky Up              | Next Slide            |
| 🖕 Middle Finger Up      | Exit Presentation     |
| ✌️ Index + Middle Finger | Show Pointer          |
| ☝️ Index Finger          | Drawing Mode          |
| 🤟 Index + Middle + Ring | Erase Last Annotation |
| 🤏 Thumb + Index Finger  | Zoom Control          |

Hand landmarks are detected in real time using the **CVZone HandTrackingModule**.

---

## 🎙️ Voice Commands

The application supports **7 voice-command actions**:

* `next` → Move to the next slide
* `previous` / `back` → Move to the previous slide
* `slide 5` → Jump directly to a specific slide
* `zoom in` → Increase zoom
* `zoom out` → Decrease zoom
* `reset zoom` → Reset zoom
* `exit` / `quit` → Exit the presentation

Voice input is captured through the microphone and converted into text using SpeechRecognition and Google Speech Recognition.

---

## ✏️ Presentation Annotation

The system provides real-time virtual drawing functionality.

* Uses the index finger to enter drawing mode.
* Tracks finger coordinates to create annotations.
* Connects consecutive coordinates to generate continuous drawings.
* Supports annotation removal through a dedicated gesture.

---

## 🔍 Dynamic Zoom Control

The project implements gesture-based zoom control using the distance between the thumb and index finger.

As the distance changes, the application dynamically adjusts the presentation zoom level.

Zoom can also be controlled through voice commands.

---

## 📷 Real-Time Webcam Processing

The application uses a webcam for continuous hand detection.

The camera feed is mirrored to provide a natural interaction experience, while a webcam preview is displayed during presentation execution.

---

## 🧠 System Workflow

```text
Webcam
   ↓
Hand Landmark Detection
   ↓
Gesture Recognition
   ↓
Gesture Analysis
   ↓
┌─────────────┬──────────────┬─────────────┐
│ Navigation  │ Annotation   │    Zoom     │
└─────────────┴──────────────┴─────────────┘
                    ↓
              Presentation

Voice Input
     ↓
Speech Recognition
     ↓
Command Processing
     ↓
Slide / Zoom / Exit
```

---

## 🛠️ Technology Stack

* **Python**
* **OpenCV**
* **CVZone**
* **MediaPipe Hand Tracking**
* **NumPy**
* **SpeechRecognition**
* **Google Speech Recognition**
* **Webcam**

---

## 📊 Project Highlights

* **7** gesture-based presentation controls
* **7** voice-command actions
* **3** major interaction categories: navigation, annotation, and zoom
* Real-time webcam-based hand landmark detection
* Touch-free presentation interaction
* Voice-assisted presentation control

---

## 💡 Use Cases

* 🎓 Classroom presentations
* 💼 Business presentations
* 🎤 Seminars and conferences
* 🧑‍🏫 Online teaching
* 🖥️ Touch-free presentation environments
* ♿ Accessibility-oriented interfaces
* 🧪 Computer Vision demonstrations

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/Aprajita348/hand-gestured-controlled-ppt.git
cd hand-gestured-controlled-ppt
```

### 2. Install dependencies

```bash
pip install opencv-python cvzone numpy SpeechRecognition PyAudio
```

If PyAudio installation causes issues on Windows, install a compatible version for your Python environment.

---

## 📁 Configure Presentation

Update the presentation folder path in the Python file:

```python
folderPath = r"C:\path\to\your\presentation"
```

Place your presentation slide images inside the configured folder.

---

## ▶️ Run

```bash
python main.py
```

Make sure:

* Webcam is connected.
* Microphone is working.
* Presentation images are available.
* Required Python libraries are installed.

---

## 🎮 Keyboard Controls

| Key | Action                     |
| --- | -------------------------- |
| `V` | Activate voice recognition |
| `Q` | Quit application           |

---

## 🧠 Concepts Demonstrated

* Real-Time Computer Vision
* Hand Landmark Detection
* Gesture Recognition
* Speech Recognition
* Image Processing
* Webcam Processing
* Human-Computer Interaction
* Real-Time Event Handling

---

## 🔮 Future Improvements

* AI-based gesture customization
* Custom gesture creation
* Presentation timer
* Automatic slide generation
* AI-powered presentation assistant
* Gesture-based menu system
* Multi-language voice commands
* PDF and PowerPoint file support

---

## 👩‍💻 Author

**Aprajita Goswami**

B.Tech — Computer Science & Engineering
