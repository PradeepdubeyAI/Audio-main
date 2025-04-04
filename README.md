
# MediaMorphosis: Multimedia Content Converter & Translator 🎶🌐

## Overview
**MediaMorphosis** is an innovative project designed to seamlessly transform and translate your digital content. Whether you're working with HTML documents or YouTube videos, this tool leverages Google Cloud APIs and powerful open-source libraries to help you:
  
1. **Convert HTML to Audio (Text-to-Speech)** 🎤  
2. **Translate HTML Content** 🌍  
3. **Translate and Analyze YouTube Audio Content** 🎧  

This guide walks you through each step in detail, ensuring that your content is accessible and ready for a global audience!

---

## Table of Contents
- [MediaMorphosis: Multimedia Content Converter \& Translator 🎶🌐](#mediamorphosis-multimedia-content-converter--translator-)
  - [Overview](#overview)
  - [Table of Contents](#table-of-contents)
  - [Step 1: Text-to-Speech (HTML to Audio) 🎤](#step-1-text-to-speech-html-to-audio-)
    - [Detailed Steps:](#detailed-steps)
    - [Outcome:](#outcome)
  - [Step 2: HTML Translation 🌍](#step-2-html-translation-)
    - [Detailed Steps:](#detailed-steps-1)
    - [Outcome:](#outcome-1)
  - [Step 3: Audio Translation and Analysis 🎧](#step-3-audio-translation-and-analysis-)
    - [Detailed Steps:](#detailed-steps-2)
    - [Outcome:](#outcome-2)
  - [Dependencies](#dependencies)
  - [API Configuration](#api-configuration)
  - [Error Handling](#error-handling)
  - [Summary 🚀](#summary-)

---

## Step 1: Text-to-Speech (HTML to Audio) 🎤

Transform your HTML content into a high-quality audio file using Google’s Text-to-Speech API. This step is perfect for creating audio versions of web content, making your material more accessible.

### Detailed Steps:
1. **Input HTML Content**:
   - **What:** Provide an HTML file or string containing structured text (headings, paragraphs, etc.).  
   - **Why:** This serves as the basis for creating a clear and organized audio narration.
2. **Language Detection**:
   - **What:** Automatically detect the primary language using the `langdetect` library.  
   - **Why:** Ensures that the proper voice and pronunciation are applied.
3. **HTML to SSML Conversion**:
   - **What:** Convert HTML content into Speech Synthesis Markup Language (SSML).  
   - **Why:** SSML allows for better control over speech output, preserving the text structure while removing extraneous HTML tags.
4. **Voice Selection**:
   - **What:** Present a list of available voices based on the detected language.  
   - **Why:** Let users choose a voice that best fits their needs, adding a personal touch to the audio.
5. **Audio Configuration**:
   - **What:** Adjust pitch, speaking rate, and volume to fine-tune the output.  
   - **Why:** Customization options help in creating a pleasant and natural listening experience.
6. **Generate Audio**:
   - **What:** Process the SSML through the Text-to-Speech API to generate the audio file.  
   - **Why:** Converts your text into an engaging audio format.
7. **Output Verification**:
   - **What:** Save the output as `output.mp3` and play it back for quality assurance.  
   - **Why:** Ensures that the generated audio meets your expectations before further use.

### Outcome:
Your HTML content is transformed into a professionally generated audio file, making your content more inclusive and engaging.

---

## Step 2: HTML Translation 🌍

Translate the text within your HTML file to a target language while preserving its original structure and formatting.

### Detailed Steps:
1. **API Configuration**:
   - **What:** Set up Google Generative AI with your predefined API key.  
   - **Why:** This enables the translation functionality.
2. **Input HTML File**:
   - **What:** Provide the file path of the HTML document that needs translation.  
   - **Why:** The file will be processed to extract text and structure.
3. **Language Selection**:
   - **What:** Choose the target language from a menu of options.  
   - **Why:** Allows for translation into the language of your choice.
4. **Create Translation Prompt**:
   - **What:** Construct a prompt that instructs the AI to translate only the text within HTML tags.  
   - **Why:** Ensures the original HTML structure is preserved while text is translated.
5. **Model Translation**:
   - **What:** Send the prompt to the AI model and receive the translated content.  
   - **Why:** Produces an accurate translation that maintains the integrity of the original document.
6. **Output File**:
   - **What:** Save the translated content to a new file (e.g., `Translated_hi.html`).  
   - **Why:** Creates a distinct version of the document that reflects the chosen target language.

### Outcome:
You receive an HTML file with translated text that preserves the original formatting—ideal for multilingual web applications.

---

## Step 3: Audio Translation and Analysis 🎧

Convert and translate audio from a YouTube video into your target language. This process involves transcription, translation, and text-to-speech conversion to create an audio file that caters to a global audience.

### Detailed Steps:
1. **Download YouTube Audio**:
   - **What:** Use `yt_dlp` to download the audio from a YouTube video as a `.wav` file.  
   - **Why:** Ensures you have a local copy of the audio content for processing.
2. **Split Audio**:
   - **What:** Divide the audio into 10-second chunks.  
   - **Why:** Makes processing more efficient and compatible with API requirements.
3. **Transcribe Audio**:
   - **What:** Use Google Cloud Speech-to-Text API to convert audio chunks into text.  
   - **Why:** Transcription is essential for further translation.
4. **Translate Transcription**:
   - **What:** Utilize Google Generative AI to translate the transcribed text into the target language.  
   - **Why:** Bridges the language gap, making content accessible to non-native speakers.
5. **Convert Translation to SSML**:
   - **What:** Process the translated text into SSML format.  
   - **Why:** Prepares the text for a high-quality text-to-speech conversion.
6. **Voice Selection and Audio Configuration**:
   - **What:** Choose the preferred voice and adjust pitch, rate, and volume.  
   - **Why:** Customization enhances the listening experience.
7. **Generate Audio**:
   - **What:** Convert the SSML text to audio using Google Text-to-Speech API.  
   - **Why:** Finalizes the process by creating a translated audio file.
8. **Output Verification**:
   - **What:** Save the final audio as `output_audio.mp3` and verify its quality.  
   - **Why:** Ensures the output meets quality standards before distribution.

### Outcome:
A polished audio file in the target language is generated from YouTube content, expanding your content’s reach to a broader audience.

---

## Dependencies

Before running MediaMorphosis, ensure the following packages are installed:
- `google-cloud-texttospeech`
- `gradio`
- `pydub`
- `langdetect`
- `pytube`
- `yt_dlp`
- `librosa`
- `soundfile`

---

## API Configuration

- **Google Cloud Credentials:**  
  Set up and configure your Google Cloud credentials to access Text-to-Speech and Speech-to-Text APIs.

- **API Keys:**  
  Ensure that you have valid API keys for both Google Generative AI and Google Cloud services.

---

## Error Handling

- **File Paths:**  
  Validate file paths to ensure they exist before processing.
  
- **Language Support:**  
  Handle unsupported languages gracefully and provide user-friendly messages.
  
- **API Retries:**  
  Implement retry logic for API calls in case of transient errors.

---

## Summary 🚀

**MediaMorphosis** offers a comprehensive workflow for converting and translating multimedia content. By following these detailed steps, you can:
- Convert HTML content to audio files.
- Translate HTML documents while retaining original formatting.
- Process and translate YouTube audio content into accessible, multilingual audio files.

Transform your content with **MediaMorphosis** and effortlessly reach audiences around the world! 🌟

---