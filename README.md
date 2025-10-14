# 🛡️ AI Guard Agent — Intelligent Room Security System  

This repository contains the complete implementation of an **AI-based security agent** capable of **voice activation**, **face recognition**, and **intelligent intruder interaction**.  
Developed as a three-stage project, the system evolves from simple speech activation to a fully integrated **autonomous guard** that recognizes trusted users and communicates with intruders using **Shakespearean-style dialogue** powered by LLMs.

---

## 🚀 Project Overview  

| Milestone | Objective | Key Features |
|------------|------------|---------------|
| **Milestone 1: Activation and Basic Input** | Enable the agent to activate upon a voice command | Speech Recognition (ASR), fuzzy matching for robust activation, basic state management |
| **Milestone 2: Face Recognition and Trusted User Enrollment** | Implement trusted user recognition using facial embeddings | Face detection, encoding & comparison, HEIC support, multi-image enrollment |
| **Milestone 3: Escalation Dialogue and Full Integration** | Handle intruders through escalating Shakespearean conversations | LLM-based dialogue system, Text-to-Speech synthesis, full video + audio integration |

---

## 📂 Repository Structure  

📁 AI-Guard-Agent/
│
├── 📓 main_notebook.ipynb # Full implementation covering all milestones
│
├── 📦 activation_audio.zip # Audio files for Milestone 1 testing
├── 📦 face_training_images.zip # Trusted user training images (Milestone 2)
├── 📦 face_testing_images.zip # Test images for recognition validation (Milestone 2)
├── 📦 final_video.zip # Test video for full system integration (Milestone 3)
│
└── 📄 README.md # This file

---

## 🧩 Milestone Details  

### 🥇 Milestone 1: Activation and Basic Input  
**Goal:** Activate the system using a spoken command such as **“Guard my room.”**

**Core Features:**
- Speech recognition with Google Speech API  
- Fuzzy string matching using `thefuzz` for robust activation  
- Automated activation test suite with multiple input audios  

**Deliverables:**
- 90%+ command recognition accuracy  
- Video demonstration of activation  

**Libraries Used:**  
`SpeechRecognition`, `ffmpeg-python`, `thefuzz`

---

### 🥈 Milestone 2: Face Recognition and Trusted User Enrollment  
**Goal:** Detect and identify trusted users while flagging unknown individuals.  

**Core Features:**
- Face recognition using the `face_recognition` library (built on dlib)  
- Multi-image and batch enrollment of trusted users  
- Persistent face encoding storage using `pickle`  
- Support for HEIC/HEIF image formats (iPhone-compatible)  
- Adjustable tolerance levels for recognition strictness  
- Choice between HOG (fast) and CNN (accurate) models  

**Deliverables:**
- Accurate recognition across 5+ varied test images  
- Demo script + explanation of facial embedding comparison  

**Libraries Used:**  
`face_recognition`, `opencv-python`, `numpy`, `pillow`, `pillow-heif`, `matplotlib`, `pickle`

---

### 🥉 Milestone 3: Escalation Dialogue and Full Integration  
**Goal:** Build an intelligent escalation dialogue system to handle intruders dynamically.  

**Core Features:**
- Integration with **LLMs (Llama3 via Ollama)** for Shakespearean-style speech  
- Four escalation levels: *Curious → Stern → Angry → Furious*  
- Dynamic Text-to-Speech (TTS) generation using `gTTS` and `pydub`  
- Real-time video processing for detecting and tracking faces  
- Activation through voice + video → dialogue → emotional TTS response  

**Deliverables:**
- Full working integration of all modules  
- Architecture diagram and test video showing system behavior  
- Coherent escalation logic with at least 3 response levels  

**Libraries Used:**  
`ollama`, `gTTS`, `pydub`, `SpeechRecognition`, `moviepy`, `fuzzywuzzy`, `opencv-python`, `matplotlib`

---

## 🧠 System Architecture  

🎤 Voice Command → 🎯 Activation Detection → 👤 Face Recognition
↓
🚨 Unknown Face Detected
↓
🤖 LLM Dialogue (Shakespearean)
↓
🔊 Emotional Voice Output

---

## 🧪 Testing and Datasets  

| Dataset | Description | Used In |
|----------|--------------|----------|
| `activation_audio.zip` | Audio samples for activation phrase detection | Milestone 1 |
| `face_training_images.zip` | Known user photos for enrollment | Milestone 2 |
| `face_testing_images.zip` | Test images for recognition evaluation | Milestone 2 |
| `final_video.zip` | Integrated test video combining voice + face recognition | Milestone 3 |

