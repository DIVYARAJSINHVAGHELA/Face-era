
# 🎬 Ultimate Video & Audio Processor (ClearCap)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python)
![PyTorch](https://img.shields.io/badge/PyTorch-AI%20Vision-ee4c2c?style=for-the-badge&logo=pytorch)
![FFmpeg](https://img.shields.io/badge/FFmpeg-Required-41cd52?style=for-the-badge&logo=ffmpeg)
![Status](https://img.shields.io/badge/Status-Active-success?style=for-the-badge)

> An all-in-one, AI-powered toolkit for extracting, cleaning, and analyzing video and audio content. 

Whether you are a content creator, developer, or video editor, this tool provides an interactive Command Line Interface (CLI) to download media, completely remove background noise using advanced AI, and automatically generate highly contextual social media captions and hashtags using Vision AI.

---

## ✨ Key Features

### 🎵 Audio Processing
* **Extract Audio from URL:** Download high-quality audio directly from platforms like YouTube, Instagram, TikTok, and Twitter using `yt-dlp`.
* **Extract Audio from Local Files:** Instantly rip audio tracks from your local `.mp4`, `.mov`, `.mkv`, or `.avi` files.
* **Basic Noise Removal:** Fast background noise reduction utilizing standard `FFmpeg` filters.
* **AI-Powered Noise Removal:** Deep audio cleaning using `librosa` and `noisereduce` algorithms, offering Light, Medium, and Strong noise reduction profiles that preserve human vocal clarity.

### 🤖 AI Vision & Content Creation
* **Smart Captions:** Analyzes your file names and categories to automatically generate catchy captions and trending hashtags (e.g., #Tech, #Nature, #Gaming).
* **AI Video Analysis (Vision AI):** Extracts key frames from your video and feeds them into a powerful machine-learning model (**Salesforce BLIP**) to deeply understand the visual context. It then generates hyper-accurate captions and dynamic hashtags tailored exactly to what happens in your video.

### 🛠️ Built-in Utilities
* **Automatic Dependency Manager:** Automatically detects missing Python packages and installs them for you on startup!
* **File Management:** Built-in viewer to organize your `downloads`, `processed` files, `exports`, and `frames`.
* **System Diagnostics:** Monitor your disk space, Python version, and backend dependencies (FFmpeg, Audio AI, Vision AI).

---

## 📋 Prerequisites

Before running the processor, ensure your system has the following installed:

1. **Python 3.8 or higher** (Ensure Python is added to your system PATH).
2. **FFmpeg** (Crucial for video/audio manipulation)
   * **Windows:** Download from [gyan.dev](https://www.gyan.dev/ffmpeg/builds/) or install via winget: `winget install ffmpeg`
   * **Mac:** `brew install ffmpeg`
   * **Linux:** `sudo apt install ffmpeg`

---

## 🚀 Installation & Setup

### Method 1: Using the Automated Setup Script (Windows)
The repository includes a batch file that automatically creates an isolated virtual environment and installs all required dependencies.

1. Clone the repository:
   ```bash
   git clone [https://github.com/YOUR-USERNAME/Video-Audio-Processor.git](https://github.com/YOUR-USERNAME/Video-Audio-Processor.git)
   cd Video-Audio-Processor
Run the setup script:

DOS
setup.bat
Activate the environment:

DOS
video_processor_env\Scripts\activate
Method 2: Manual Installation
Clone the repository and navigate to the directory.

Install the required Python packages:

Bash
pip install -r requirements.txt
(Note: If you skip this, main.py has a built-in fallback that will attempt to auto-install missing packages when you first run it!)

🎮 Usage
Start the interactive CLI application by running the main script:

Bash
python main.py
Main Menu Overview
Upon launching, you will be greeted by the interactive terminal menu:

Plaintext
    ╔═══════════════════════════════════════════════╗
    ║           ULTIMATE VIDEO PROCESSOR            ║
    ║              All-in-One Edition               ║
    ╚═══════════════════════════════════════════════╝
    Features: FFmpeg | AudioAI | VisionAI

🔧 MAIN MENU - Choose an option:

🎵 AUDIO PROCESSING:
  1. Extract Audio from Video URL
  2. Extract Audio from Local File
  3. Remove Noise (Basic - FFmpeg)
  4. Remove Noise (AI Powered)

📝 CONTENT CREATION:
  5. Generate Smart Captions
  6. Generate AI Captions (Video Analysis)

🛠️ UTILITIES:
  7. File Manager
  8. System Information
  9. Cleanup Temporary Files
  0. Exit
Simply type the number of the operation you want to perform and follow the on-screen prompts!

📁 Project Structure
Plaintext
📦 Video-Audio-Processor
 ┣ 📂 utils/                # Utility scripts (file validation, sanitization)
 ┃ ┗ 📜 file_utils.py
 ┣ 📜 main.py               # The primary entry point & interactive CLI
 ┣ 📜 requirements.txt      # Python package dependencies
 ┣ 📜 setup.bat             # Windows auto-setup script
 ┣ 📜 advanced_audio.py     # Legacy/Modular advanced audio logic
 ┣ 📜 advanced_video.py     # Legacy/Modular advanced video logic
 ┗ 📜 .gitignore            # Git ignore configurations
🧠 Note on AI Models
If you utilize the Generate AI Captions (Video Analysis) feature, the application relies on the Hugging Face transformers library to download the Salesforce/blip-image-captioning-base model.

First Run: The initial run of this specific feature will require a one-time download of approximately 1.4 GB. Please be patient as the model caches to your local machine.

🤝 Contributing
Contributions, issues, and feature requests are welcome!
Feel free to check out the issues page.

Fork the Project

Create your Feature Branch (git checkout -b feature/AmazingFeature)

Commit your Changes (git commit -m 'Add some AmazingFeature')

Push to the Branch (git push origin feature/AmazingFeature)

Open a Pull Request

📝 License
Distributed under the MIT License. See LICENSE for more information.
