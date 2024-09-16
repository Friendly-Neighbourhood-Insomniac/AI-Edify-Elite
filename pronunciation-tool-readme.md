# Pronunciation Practice Tool

## Overview
This Pronunciation Practice Tool is a web application that helps users improve their English pronunciation. It generates text for users to read aloud, records their voice, transcribes the audio, and provides feedback on their pronunciation.

## How It Works

### 1. Text Generation
- The app uses OpenAI's GPT-3.5-turbo model to generate two simple sentences for the user to practice.
- This is done through the `generate_text()` function, which sends a request to the OpenAI API.

### 2. Audio Recording
- Users can record their voice directly in the web interface using the Gradio audio component.

### 3. Speech-to-Text Transcription
- The `transcribe_audio_realtime()` function uses the SpeechRecognition library to convert the user's audio into text.
- It specifically uses Google's speech recognition service for transcription.

### 4. Pronunciation Feedback
- The `get_pronunciation_feedback()` function compares the original text with the transcribed text.
- It uses another OpenAI API call to generate helpful feedback on the user's pronunciation.

### 5. User Interface
- The interface is built using Gradio, which provides an easy-to-use web interface.
- It includes buttons for generating new text and submitting recordings, as well as text areas for displaying the text to read, transcription, and feedback.

## Setup and Running

1. Clone the repository
2. Install required packages:
   ```
   pip install gradio openai SpeechRecognition
   ```
3. Set up your OpenAI API key as an environment variable:
   ```
   export OPENAI_API_KEY='your-api-key-here'
   ```
4. Run the application:
   ```
   python app.py
   ```

## Dependencies
- gradio
- openai
- SpeechRecognition

## Limitations and Future Improvements
- The app currently relies on an internet connection for API calls and speech recognition.
- Error handling could be improved for a more robust user experience.
- The feedback system could be enhanced with more detailed phonetic analysis.
- User data is not stored, so there's no progress tracking between sessions.

## Notes
This is my first major project using APIs and speech recognition. Any feedback or contributions are welcome!

