# whisper-audio-to-text
A simple implementation of OpenAI’s Whisper for transcribing MP3 files on Google Colab.

Here's the **final enhanced README.md** with the **updated usage instructions** explaining both **uploading a custom file** and **using the sample file** from GitHub.  

---

# **Whisper Audio-to-Text (Google Colab)**  

[![Python](https://img.shields.io/badge/Python-3.7+-blue.svg)](https://www.python.org/)  
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Compatible-orange?logo=googlecolab)](https://colab.research.google.com/)  
[![OpenAI Whisper](https://img.shields.io/badge/OpenAI-Whisper-brightgreen?logo=openai)](https://github.com/openai/whisper)  
[![License](https://img.shields.io/github/license/asadsandhu/whisper-audio-to-text)](LICENSE)  

---

## 🚀 **Overview**  
This repository provides a **Google Colab-based implementation** of OpenAI’s **Whisper AI** for transcribing audio files into text.  
Simply **clone the repo, run the notebook, upload an audio file, and get an accurate transcription in seconds!**  

✅ **No setup required** – Just open the `.ipynb` file in Colab  
✅ **User-friendly** – Upload an audio file, run a single command, and get transcriptions  
✅ **Supports multiple languages** with the **Whisper `medium` model**  
✅ **Works with multiple audio formats** including MP3, WAV, M4A, and FLAC  

---

## 📌 **Supported Audio Formats**  
Whisper AI supports a variety of common audio formats. You can upload files in any of the following formats:  

| **Format** | **File Extension** | **Description** |
|------------|--------------------|----------------|
| **MP3** | `.mp3` | Compressed audio format, widely used |
| **WAV** | `.wav` | High-quality, uncompressed audio |
| **M4A** | `.m4a` | Common format for iOS recordings |
| **FLAC** | `.flac` | Lossless audio format, high fidelity |

💡 **Note:** Files in other formats can be converted using FFmpeg before transcription.

---

## 📖 **How to Use**  

### **1️⃣ Clone This Repository in Google Colab**  
Open a new Colab notebook and run the following:  

```bash
!git clone https://github.com/asadsandhu/whisper-audio-to-text.git
%cd whisper-audio-to-text
```

### **2️⃣ Install Required Dependencies**  
Run the following commands one by one to set up **Whisper AI** and **FFmpeg**:  

```bash
# Install Whisper AI
!pip install git+https://github.com/openai/whisper.git
```

```bash
# Install FFmpeg (required for audio processing)
!sudo apt update && sudo apt install ffmpeg
```

---

### **3️⃣ Upload an Audio File (Optional - Skip if using Sample.mp3)**  
If you **want to transcribe your own audio file**, run this in a Colab cell:  

```python
from google.colab import files
uploaded = files.upload()
```

🔹 **After uploading your file, remember its name.**  
🔹 **In step 5, replace `"Sample.mp3"` with the name of your uploaded file.**  

---

### **4️⃣ (Alternative) Use the Sample Audio File (Skip if you uploaded your own)**  
If you **don’t want to upload a file** and just want to test Whisper AI, run this command:  

```bash
!wget https://github.com/asadsandhu/whisper-audio-to-text/raw/main/Sample.mp3 -O Sample.mp3
```

🔹 This will **automatically download** a sample MP3 file (`Sample.mp3`) from GitHub.  
🔹 **If you already uploaded a file, skip this step.**  

---

### **5️⃣ Run Whisper AI for Transcription**  
Now, transcribe the audio file with Whisper:  

```bash
!whisper "Sample.mp3" --model medium
```

🔹 **If you uploaded your own file in step 3**, replace `"Sample.mp3"` with **your file name**.  
🔹 **You can change the model** by replacing `medium` with any of the available Whisper models.  

#### **Available Whisper Models & Their Performance**  

| **Model** | **Size** | **Speed** | **Accuracy** | **Best For** |
|-----------|---------|----------|--------------|--------------|
| `tiny`    | 39 MB   | 🚀 Very Fast  | ❌ Low Accuracy  | Quick testing, low-end devices |
| `base`    | 74 MB   | ⚡ Fast  | 🔸 Moderate Accuracy | Short recordings, general use |
| `small`   | 244 MB  | ⚡ Moderate  | 🔹 Good Accuracy  | Standard transcription tasks |
| `medium`  | 769 MB  | ⏳ Slower  | ✅ High Accuracy | Most users, multilingual support |
| `large`   | 1550 MB | 🕒 Slowest  | 🔥 Best Accuracy | Research, high-quality needs |

🔹 **Larger models provide better accuracy but take longer to process**.  
🔹 **If speed is a priority**, use `small` or `base`. If accuracy is **more important**, use `medium` or `large`.  
🔹 **Example: Using the large model**  

```bash
!whisper "Sample.mp3" --model large
```

---

## 💡 **Example Usage Flow**  

| **Scenario** | **Steps to Follow** |
|-------------|----------------------|
| **Upload your own audio file** | Run **Step 3** → Skip **Step 4** → Run **Step 5** (rename file) |
| **Use the sample audio file** | Skip **Step 3** → Run **Step 4** → Run **Step 5** |

---

## 🔊 **Sample File for Testing**  
A sample MP3 file (`Sample.mp3`) is included in this repository for quick testing. You can use it to check the functionality before uploading your own files.  

---

## 📌 **Requirements**  
- **Google Colab** (Runs in the cloud, no local installation needed)  
- **Python 3.7+**  
- **Whisper AI** (`pip install whisper`)  
- **FFmpeg** (pre-installed in Colab)  

---

## 🎯 **Why Use This Repository?**  
✔ **Minimal Effort** – Just upload and run, no extra configurations  
✔ **Highly Accurate** – Uses Whisper’s `medium` model for precise transcriptions  
✔ **Cloud-Based** – Runs on **Google Colab’s free GPU resources**  
✔ **Multiple Formats** – Supports MP3, WAV, M4A, FLAC  

---

## 🤝 **Contributing**  
Contributions are welcome! If you find any issues or have ideas for improvements, feel free to submit a **pull request** or open an **issue**.  

---

## 📜 **License**  
This project is licensed under the **MIT License**.  

---

### 🔗 **Connect with Me**  
If you find this repository helpful, feel free to **star 🌟 it on GitHub**! 🚀  

---
