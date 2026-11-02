# 🎙️ Voice-Based Gender Classification Engine

An artificial intelligence pipeline and web application designed to extract acoustic properties from human speech audio signals and accurately classify the speaker's gender (Male/Female) using optimized Machine Learning algorithms. 

---

## 💡 Key Features
- **Acoustic Signal Processing:** Leverages specialized audio engineering principles to ingest, clean, and extract high-dimensional vocal features from raw audio inputs.
- **Robust Feature Engineering:** Extracts critical speech features including fundamental frequencies, spectral patterns, pitch variations, and acoustic amplitudes.
- **Production-Ready ML Pipeline:** Implements standalone components for dataset processing, pipeline scaling, model training, and serial generation of model weights.
- **Interactive REST API & Web GUI:** Includes a fast web server framework and a minimal frontend dashboard allowing users to record or upload live audio files for real-time inference.

---

## 🛠️ Tech Stack & Libraries
- **Language:** Python 3.11+
- **Audio Processing:** Librosa, Soundfile
- **Machine Learning Pipeline:** Scikit-learn (SVC / RandomForest / Logistic Regression)
- **Data Serialization:** Pickle (`.pkl`)
- **Backend Framework:** FastAPI, Uvicorn
- **Frontend Dashboard:** Semantic HTML5, CSS3 Grid layouts, Vanilla JavaScript Web Audio API

---

## 📂 Project Directory Structure

Based on the operational repository setup, the code artifacts are organized cleanly into logical application layers:

```text
voice_recoginition_assighnment/voicedataset/
├── data/
│   └── voice.csv                # Ingested dataset containing tabular acoustic features
├── model_assets/
│   ├── gender_model.pkl         # Trained and serialized classifier weights
│   ├── label_encoder.pkl        # Encoded target categorical variables
│   └── scaler.pkl               # Serialized StandardScaler for structural transforms
├── static/
│   ├── css/
│   │   └── style.css            # Minimal frontend dashboard layout definitions
│   └── js/
│   │   └── script.js            # In-browser microphone recorder & audio processing logic
├── analyze_features.py          # Descriptive statistical analysis script
├── audio_processor.py           # Core audio feature extraction and Librosa mapping script
├── api.py / predict.py          # FastAPI server handling file routing & model inference
├── train.py                     # Training execution pipeline 
├── index.html                   # Interactive main browser application page
└── .gitignore                   # Safe deployment definitions for local virtual environments
```

---

## 🚀 Local Installation & Execution Guide

Follow these sequential steps to boot the application up locally on your computer:

### 1. Clone the Project Files
```bash
git clone https://github.com
cd voice-gender-classification
```

### 2. Activate Virtual Environment & Dependencies
Initialize your isolated local runtime environment and populate it with required packages:
```bash
# On Windows
python -m venv .venv
.venv\Scripts\activate

# On macOS/Linux
python3 -m venv .venv
source .venv/bin/activate

# Install essential operational dependencies
pip install fastapi uvicorn librosa numpy pandas scikit-learn soundfile
```

### 3. Run the Training Pipeline
If you wish to re-train the architecture or configure the serialized model parameters manually, run the training pipeline script:
```bash
python train.py
```
*This updates the `gender_model.pkl`, `scaler.pkl`, and `label_encoder.pkl` artifacts inside the `model_assets/` subdirectory.*

### 4. Deploy the Local Server
Boot up the integrated FastAPI server framework to preview your app interactively:
```bash
uvicorn api:app --reload
```
*Once running, navigate your web browser directly to `http://127.0.0.1:8000` to interact with the Voice Gender Classification dashboard or upload audio samples.*

---

## 🧠 Engineering & Contributor Credits
- **Bezawit Degu** - AI/ML Engineer ([@BezawitDegu](https://github.com))
- Developed proudly as a core portfolio deployment showcasing end-to-end signal processing and machine learning operationalization.
