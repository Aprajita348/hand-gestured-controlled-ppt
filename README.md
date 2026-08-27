# hand-gestured-controlled-ppt
# 🖐️ AI-Based Gesture & Voice Controlled Presentation System

An interactive **computer vision-based presentation controller** that allows users to control presentation slides using **hand gestures and voice commands** instead of a keyboard or mouse.

The system uses a webcam to detect hand movements in real time and provides features such as slide navigation, pointer control, drawing/annotation, zooming, and voice-based commands.

---

## 🚀 Features

### 🖐️ Hand Gesture Control

Control your presentation using different hand gestures:

| Gesture                  | Action                |
| ------------------------ | --------------------- |
| 👍 Thumb Up              | Previous Slide        |
| 🤙 Pinky Up              | Next Slide            |
| 🖕 Middle Finger Up      | Exit Presentation     |
| ✌️ Index + Middle Finger | Show Pointer          |
| ☝️ Index Finger          | Drawing Mode          |
| 🤟 Index + Middle + Ring | Erase Last Annotation |
| 🤏 Thumb + Index Finger  | Zoom Control          |

The system detects hand landmarks using **CVZone HandTrackingModule**.

---

## 🎙️ Voice Commands

The presentation can also be controlled using voice commands.

Press **`V`** to activate voice recognition.

Supported commands include:

* `next` → Move to the next slide
* `previous` / `back` → Move to the previous slide
* `slide 5` → Jump directly to slide 5
* `zoom in` → Increase zoom
* `zoom out` → Decrease zoom
* `reset zoom` → Reset zoom
* `exit` / `quit` → Exit the presentation

Speech is captured through the microphone and converted into text using SpeechRecognition and Google speech recognition.

---

## ✏️ Presentation Annotation

The application provides a virtual drawing feature.

By raising the **index finger**, the user can draw directly over the presentation slide.

The system stores the finger coordinates and connects consecutive points to create annotations.

The last annotation can be removed using the erase gesture.

---

## 🔍 Zoom Control

The system supports interactive zooming using the distance between the **thumb and index finger**.

As the distance between the fingers changes, the zoom level is calculated dynamically.

The zoom range is limited to prevent excessive scaling.

Voice commands can also be used for zooming.

---

## 📷 Webcam Integration

The webcam is used for real-time hand detection.

The camera feed is mirrored to provide a more natural interaction experience.

A small webcam preview is also displayed on the presentation slide while the application is running.

---

## 🛠️ Technologies Used

* **Python**
* **OpenCV**
* **CVZone**
* **MediaPipe Hand Tracking** (through CVZone)
* **NumPy**
* **SpeechRecognition**
* **Google Speech Recognition**
* **Webcam**

---

## 📂 Project Structure

```text
Gesture-Voice-Presentation/
│
├── main.py
├── presentation/
│   ├── slide1.jpg
│   ├── slide2.jpg
│   ├── slide3.jpg
│   └── ...
│
├── README.md
└── requirements.txt
```

> The presentation folder should contain the slide images that the application will display.

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/gesture-voice-presentation.git
cd gesture-voice-presentation
```

### 2. Install Required Libraries

```bash
pip install opencv-python cvzone numpy SpeechRecognition PyAudio
```

If PyAudio causes installation problems on Windows, install a compatible PyAudio package for your Python version.

---

## 📁 Configure Presentation Folder

Update the presentation folder path in the Python file:

```python
folderPath = r"C:\path\to\your\presentation"
```

Replace it with the location of your own slide images.

The application automatically loads the images from this folder.

---

## ▶️ Run the Project

Start the application using:

```bash
python main.py
```

Make sure:

* Your webcam is connected.
* Your microphone is working.
* Presentation images are present in the configured folder.
* The required Python libraries are installed.

---

## 🎮 Keyboard Controls

| Key | Action                 |
| --- | ---------------------- |
| `V` | Activate voice command |
| `Q` | Quit application       |

The program continuously checks keyboard input while the presentation is running.

---

## 🔄 How It Works

```text
              ┌─────────────────┐
              │     Webcam      │
              └────────┬────────┘
                       ↓
              ┌─────────────────┐
              │ Hand Detection  │
              │   CVZone        │
              └────────┬────────┘
                       ↓
              ┌─────────────────┐
              │ Gesture Analysis│
              └────────┬────────┘
                       ↓
        ┌──────────────┼──────────────┐
        ↓              ↓              ↓
   Navigation      Annotation       Zoom
        │              │              │
        └──────────────┼──────────────┘
                       ↓
                Presentation


          🎙️ Voice Input
                ↓
        Speech Recognition
                ↓
         Command Processing
                ↓
       Slide / Zoom / Exit
```

---

## 💡 Use Cases

This project can be useful for:

* 🎓 Classroom presentations
* 💼 Business presentations
* 🎤 Seminars and conferences
* 🧑‍🏫 Online teaching
* 🖥️ Touch-free presentation environments
* ♿ Accessibility-oriented interfaces
* 🧪 Computer Vision demonstrations

---

## 🔮 Future Improvements

Possible future enhancements include:

* AI-based gesture customization
* More voice commands
* Custom gesture creation
* Presentation timer
* Automatic slide generation
* AI-powered presentation assistant
* Gesture-based menu system
* Multi-language voice commands
* Better zoom-center tracking
* Support for PDF and PowerPoint files directly

---

## 🧠 Key Concepts Demonstrated

This project demonstrates practical implementation of:

* Real-time Computer Vision
* Hand Landmark Detection
* Gesture Recognition
* Speech Recognition
* Image Processing
* Webcam Processing
* Human-Computer Interaction
* Real-time Event Handling

---

## 👩‍💻 Author

**Aprajita Goswami**

B.Tech Student

---

## ⭐ If You Like This Project

If you found this project useful or interesting, consider giving the repository a ⭐ on GitHub!
