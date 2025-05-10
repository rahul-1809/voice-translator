## Live Speech Translator

This project is a real-time speech-to-speech translation application built using **Streamlit**, **Google Generative AI (Gemini)** for translation, **SpeechRecognition** for voice-to-text, and **gTTS** for text-to-speech synthesis.

### Features

* Voice recording from microphone
* Speech-to-text recognition using Google Speech API
* Language translation using Google Gemini (via `google.generativeai`)
* Text-to-speech conversion using gTTS
* Support for over 20 languages
* Downloadable audio output in MP3 format

### Supported Languages

* English, Hindi, Bengali, Telugu, Marathi, Tamil, Urdu, Gujarati, Malayalam, Kannada, Punjabi
* Spanish, French, German, Chinese (Simplified), Japanese, Korean, Russian, Portuguese, Arabic, Italian, Dutch, Turkish


### Tech Stack

* **Frontend**: Streamlit
* **Speech Recognition**: SpeechRecognition with Google Speech API
* **Translation**: Gemini via `google.generativeai`
* **Text-to-Speech**: gTTS
* **Audio Handling**: Streamlit's audio player and `BytesIO`


### Installation Instructions

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/live-speech-translator.git
   cd live-speech-translator
   ```

2. **Create and Activate a Virtual Environment (Optional but Recommended)**

   ```bash
   python -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

4. **Set Up API Key** Create a file named `.streamlit/secrets.toml` and add your Gemini API key:

   ```
   [general]
   GEMINI_API_KEY = "your-gemini-api-key-here"
   ```


### Running the Application

Use the following command to launch the app locally:

```bash
streamlit run app.py
```

Once started, a browser window will open where you can:

* Select input and target languages
* Record speech using your microphone
* View the recognized and translated text
* Play the translated audio
* Download the audio as an MP3 file


### Notes

* The app uses the default microphone for input. Make sure your device's microphone is working.
* Ensure a stable internet connection as both speech recognition and translation require online APIs.


### Requirements

Here are the packages used in this project:

```txt
streamlit
google-generativeai
SpeechRecognition
gtts
pyaudio
```

If you face issues installing PyAudio on Windows:

```bash
pip install pipwin
pipwin install pyaudio
```

### License

This project is for educational and non-commercial use. Please ensure you follow Google Gemini and gTTS terms of service while using their APIs.
