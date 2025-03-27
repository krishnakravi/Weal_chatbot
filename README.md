# Weal - Mental Health Support Chatbot

Weal is an AI-powered mental health support assistant that combines voice stress analysis with conversational AI to provide personalized mental health support.

## 📋 Project Overview

Weal integrates multiple advanced technologies to create a compassionate mental health support system:

1. **Voice Stress Analysis**: Utilizes audio processing techniques to analyze voice patterns for signs of stress.
2. **Text Sentiment Analysis**: Evaluates the emotional content of the user's speech.
3. **Knowledge-Based Responses**: Provides contextually relevant information from mental health resources (DSM-5-TR).
4. **Conversational Interface**: Offers a user-friendly chat interface for seamless interaction.

## 🔍 Features

- **Voice Analysis**: Detects stress levels in voice recordings by analyzing pitch, speech rate, energy variations, and spectral features
- **Text Transcription**: Converts speech to text using the Whisper model
- **Sentiment Analysis**: Evaluates the emotional tone of transcribed speech
- **Combined Score Analysis**: Merges audio and text features to generate a comprehensive stress assessment
- **Knowledge-Based Guidance**: Provides responses grounded in mental health literature
- **Conversation Memory**: Maintains context throughout the interaction

## 🛠️ Technical Components

- **LangChain**: For document processing and conversational chains
- **FAISS**: For efficient vector similarity search
- **HuggingFace Transformers**: For sentiment analysis
- **Whisper**: For speech-to-text conversion
- **Librosa**: For audio feature extraction
- **Gradio**: For the interactive web interface

## 🔧 Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/Weal_chatbot.git
cd Weal_chatbot
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Additional dependencies that may need to be installed:
```bash
pip install gradio librosa transformers whisper matplotlib numpy pandas scikit-learn langchain-ollama
```

## 🚀 Usage

1. Make sure you have [Ollama](https://ollama.com/) installed and running with the llama2 model pulled:
```bash
# Install Ollama from ollama.com then run:
ollama pull llama2
```

2. Place your PDFs (like DSM_5_TR.pdf) in the project directory

3. Place audio files for analysis (like divyanka_stress_possible.ogg) in the project directory

4. Run the Jupyter notebook:
```bash
jupyter notebook chatbot4.ipynb
```

5. Execute the notebook cells to start the Gradio interface

## 💡 How It Works

1. **Audio Analysis Pipeline**:
   - Loads and processes audio using Librosa
   - Extracts time-domain, frequency-domain, and spectral features
   - Transcribes speech to text using Whisper
   - Performs sentiment analysis on transcribed text
   - Calculates a combined stress score

2. **Conversational Pipeline**:
   - Processes mental health reference documents using LangChain
   - Creates embeddings and vector storage using FAISS
   - Implements conversational retrieval chain with Ollama LLM
   - Provides responses based on both document knowledge and user input

3. **User Interface**:
   - Displays stress assessment results
   - Provides chat interface for ongoing conversation
   - Includes mental health resources and emergency contacts

## ⚠️ Important Note

This tool is intended for research and support purposes only. It is not a substitute for professional medical advice, diagnosis, or treatment. Always seek the advice of your physician or other qualified health provider with any questions regarding a medical condition.

