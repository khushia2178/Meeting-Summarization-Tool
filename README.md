# Meeting-Summarization-Tool
This repository provides a tool to transcribe audio from uploaded files, generate summaries, analyze sentiment, and upload the results to cloud storage (Google Drive). The tool supports audio and video files and integrates OpenAI's Whisper model for transcription, transformers for summarization, and a sentiment analysis pipeline.

# Features

1.Audio Extraction: Extracts audio from video files (e.g., .mp4).
2.Audio Transcription: Converts speech to text using OpenAI's Whisper model.
3.Summarization: Generates concise bullet-point summaries from transcripts.
4.Sentiment Analysis: Analyzes the sentiment (positive, negative, or neutral) of the transcription.
5.Cloud Storage Integration: Uploads summaries to Google Drive.
# Prerequisites

Before you begin, make sure you have the following dependencies:

1.Python 3.x 
2.Google Colab
# Libraries:
1.transformers (for transcription and summarization).
2.pydub (for audio extraction).
3.librosa (for audio processing).
4.google-api-python-client (for Google Drive integration).
# Google Drive Setup
To use Google Drive integration:

1.Go to the Google Developers Console.
2.Create a new project and enable the Google Drive API.
3.Create credentials anf get the .json key.
4.Share your Google Drive folder with the client email associated with your Google API project.
5.Add the drive folder ID where you want to store summaries to the code.
# Google Colab Integration
To run the tool in Google Colab, follow these steps:

1.Upload an audio or video file directly to Colab using the files.upload() method.
2.The tool will automatically process the file to:
3.Extract audio from videos (if applicable).
4.Transcribe the audio using OpenAI's Whisper model.
5.Generate a summary of the transcription.
5.Analyze the sentiment of the transcription.
6.Save the summary to a .txt file and upload it to Google Drive.
# File Formats
The tool supports the following file formats:

1.Audio Files: .mp3, .wav
2.Video Files: .mp4
# Process Overview
1.File Upload: Upload your audio or video file using the files.upload() method in Google Colab.
2.Audio Extraction: If the uploaded file is a video, the tool extracts the audio using pydub.
3.Transcription: The audio file is transcribed to text using OpenAI's Whisper model.
4.Summarization: A concise summary is generated using the transformers library from HuggingFace.
5.Sentiment Analysis: The sentiment (positive, negative, or neutral) of the transcript is analyzed using HuggingFace's sentiment analysis pipeline.
6.Uploading Results: The summary and sentiment results are saved to a .txt file and uploaded to your specified Google Drive folder.
# File Storage
1.The summaries are uploaded to Google Drive for cloud storage.
# Usage Instructions

Upload a File: Upload your file (audio or video) into the Colab environment. The tool will automatically process it.
# Processing Steps:
If the file is a video, the tool will extract the audio.
The tool transcribes the audio into text using Whisper.
A summary of the transcript is generated using the transformers library.
Sentiment analysis is performed on the transcription.
# Results:
1.The summary and sentiment analysis results are saved in a .txt file.
2.The file is uploaded to the specified Google Drive folder.
