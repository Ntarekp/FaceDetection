# Face Recognition System with MediaPipe and LBPH

Real-time face recognition combining **MediaPipe** for detection and **LBPH** for classical feature-based recognition.

## Features

- 🎯 Real-time face detection and recognition
- 🟢 Color-coded visualization (green = recognized, red = unknown)
- ⚡ Fast training with minimal data (30-50 images per person)
- 📊 Confidence scoring and FPS monitoring
- 🔄 Easy retraining for new people
- 💻 Cross-platform (Windows, macOS, Linux)

## Quick Start

```bash
# 1. Capture training data
python capture_training_data.py

# 2. Train the model
python train_recognizer.py

# 3. Run face recognition
python run_face_recognition.py
```

## How It Works

1. **MediaPipe Detection** - Pre-trained BlazeFace model detects faces in real-time
2. **LBPH Recognition** - Classical algorithm compares local binary patterns to identify people
3. **Pipeline** - Detected faces are cropped, converted to grayscale, and matched against trained model

---

## Installation

```bash
# Clone repository
git clone https://github.com/yourusername/face_recognition_with_mediapipe.git
cd face_recognition_with_mediapipe

# Create virtual environment (Python 3.8-3.11 required)
python3.11 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

---

## Usage

### 1. Capture Training Data

```bash
python capture_training_data.py
```

- Enter person's name
- Press **SPACE** to capture images (30-50 per person)
- Press **Q** when done
- Repeat for each person

### 2. Train Model

```bash
python train_recognizer.py
```

Trains LBPH recognizer on captured images (~1-5 seconds)

### 3. Run Recognition

```bash
python run_face_recognition.py
```

**Controls:** Q/ESC = Quit, S = Screenshot

**Confidence Scores:** 0-50 (excellent), 50-70 (good), 70+ (unknown)

---

## Technical Stack

- **MediaPipe** - BlazeFace for face detection (~30-60 FPS)
- **LBPH** - Local Binary Patterns Histograms for recognition
- **OpenCV** - Image processing and computer vision
- **Python 3.8-3.11** - Core programming language

---

**⭐ Star this repo if you find it useful!**
