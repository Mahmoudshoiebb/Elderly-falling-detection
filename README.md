# Elderly Fall Detection using MediaPipe

**Author:** Mahmoud M. Shoieb  

---

## Project Overview

This project detects falls in real-time using a webcam feed and **MediaPipe Pose Estimation**. The model captures body landmarks of a person standing in front of the camera, calculates key angles (such as torso, leg, and head tilt), and determines whether the person has fallen or not.  

It aims to provide a lightweight and efficient fall detection system suitable for elderly care environments where immediate alerts can save lives.  

> The system relies on **computer vision** and **pose-based angle calculation** instead of heavy deep-learning models, making it fast and deployable on modest hardware.

---

## Table of Contents
- [Overview](#project-overview)
- [Demo](#demo)
- [Tech Stack](#tech-stack)
- [Repository Structure](#repository-structure)
- [Setup / Installation](#setup--installation)
- [How to Run](#how-to-run)
- [Methodology](#methodology)
- [My Contributions](#my-contributions)
- [Acknowledgements](#acknowledgements)
- [License](#license)
- [Contact](#contact)

---

## Demo

<img src="docs/demo.gif" alt="Fall Detection Demo" width="600"/>


---

## Tech Stack
- **Language:** Python 3.8+  
- **Libraries:**  
  - `mediapipe` – Pose detection framework  
  - `opencv-python` – Video capture and image processing  
  - `numpy` – Numerical computations and angle calculations  
  - `matplotlib` (optional) – Visualization  
- **Hardware:** Any device with a webcam (laptop, USB camera, or Raspberry Pi camera)

---

## Repository Structure
```
Elderly-Fall-Detection/
├─ notebooks/
│  └─ Elderly_falling_detection.ipynb
├─ docs/
│  └─ Elderly_Falling_Detection_Report.pdf
├─ src/
│  └─ fall_detection.py        # optional: real-time detection script
└─ README.md
```

---

## Setup / Installation

**1. Clone the repository**
```bash
git clone https://github.com/Mahmoudshoiebb/Elderly-falling-detection.git
cd Elderly-Fall-Detection
```

**2. Create a virtual environment**
```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS/Linux
source venv/bin/activate
```

**3. Install dependencies**

install manually:
```bash
pip install opencv-python mediapipe numpy matplotlib
```

---

## How to Run

### Option 1 – Run the Notebook
Open the notebook:
```bash
jupyter notebook notebooks/Elderly_falling_detection.ipynb
```
Then run all cells to see fall detection results using your webcam.

### Option 2 – Run Python Script 
If you’ve exported logic into a `.py` file:
```bash
python src/fall_detection.py
```

Press `q` to quit webcam preview.

---

## Methodology

1. **Pose Detection:**  
   Uses MediaPipe’s Pose model to extract 33 key body landmarks (shoulders, hips, knees, etc.).  
2. **Angle Calculation:**  
   Computes relative angles between joints to measure orientation and posture stability.  
3. **Fall Condition Detection:**  
   If certain angle thresholds or body orientations indicate loss of balance (e.g., torso near-horizontal), the system classifies it as a *fall event*.  
4. **Output:**  
   Displays “Fall Detected” on the frame in real-time and can be extended to trigger alerts.

---

## My Contributions
This project was fully developed by **Mahmoud M. Shoieb**, including:
- Research and design of pose-based fall detection method.  
- Implementation using MediaPipe and OpenCV.  
- Real-time detection logic and threshold tuning.  
- Report writing and experiment documentation.  

---

## Acknowledgements
- [Google MediaPipe](https://mediapipe.dev/) for pose estimation library.
- OpenCV community for computer vision tools.  
- No collaborators — individual project.

---

## License
This repository is distributed under the MIT License.  
See the [LICENSE](LICENSE) file for more details.

---

## Contact
**Mahmoud M. Shoieb**  
GitHub: https://github.com/Mahmoudshoiebb 
Email: mahmoudshoieb12@gmail.com

