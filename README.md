# AI Voice-Based Debate Partner 🎙️🧠

## Overview
This project is a real-time, voice-based AI system developed as part of the **Pak-Angels HEC Generative AI Training Program**. It is designed to act as an intelligent debate partner. Users speak their arguments directly into the microphone, and the AI processes the speech, generates a logical counter-argument, and responds back using a synthesized voice.

The project utilizes a modern architecture divided into a React frontend interface and a powerful FastAPI backend pipeline.

## Core Pipeline & Features
1. **Audio Input:** User speaks via a clean UI built with React + Vite.
2. **Audio Processing:** Raw audio (`.webm`) is securely sent to the backend, converted to 16kHz mono `.wav`, and processed for noise reduction and silence stripping.
3. **Speech-to-Text:** The clean audio is transcribed using OpenAI's Whisper model for high accuracy.
4. **AI Logic (LLM):** The transcribed text is sent to an LLM (Llama-3.1-8b-instant via Groq API) to generate logical debate responses and counter-arguments.
5. **Voice Output (TTS):** The AI's response is converted back into speech and played seamlessly to the user.

## Tech Stack
* **Frontend:** React, Vite, Tailwind CSS
* **Backend:** Python, FastAPI
* **AI Models:** OpenAI Whisper (Base), Llama 3.1 8b (Groq API)
* **Audio Tools:** pydub, noisereduce, pyaudio

## Getting Started (Local Setup)
Ensure you have `ffmpeg` installed on your system for audio processing.

**1. Clone the repository:**
```bash
git clone [https://github.com/YourUsername/AI-Voice-Debate-Partner.git](https://github.com/YourUsername/AI-Voice-Debate-Partner.git)
```

**2. Backend Setup:**
```bash
cd debate_backend
pip install -r requirements.txt
uvicorn app:app --reload
```

**3. Frontend Setup:**
```bash
cd ai-debate-partner
npm install
npm run dev
```
