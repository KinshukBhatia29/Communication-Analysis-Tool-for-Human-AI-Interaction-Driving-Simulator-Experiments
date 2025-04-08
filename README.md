# Communication Analysis Tool for Human-AI Interaction in Driving Simulator Experiments

## Overview

This repository provides a complete pipeline for analyzing human-AI interaction in driving simulator experiments. It processes audiovisual data to extract insights using:

- *Speech-to-Text Transcription*: Converts spoken dialogue from audio files into text.
- *Speaker Diarization*: Identifies and labels different speakers.
- *Sentiment Analysis*: Determines the emotional tone of speech segments.
- *Named Entity Recognition (NER)*: Extracts relevant named entities from transcriptions.
- *Visualization*: Generates various graphs to analyze conversation patterns.

## Prerequisites

### 1. Clone the Repository

bash
git clone https://github.com/KinshukBhatia29/Communication-Analysis-Tool-for-Human-AI-Interaction-Driving-Simulator-Experiments.git
cd Communication-Analysis-Tool-for-Human-AI-Interaction-Driving-Simulator-Experiments


### 2. Install Dependencies

- For transcription, diarization, and sentiment analysis:
  bash
  pip install -r requirement_transcription.txt
  
- For visualization:
  bash
  pip install -r requirement_visualization.txt
  

### 3. Set Up Hugging Face API Token

This project uses Hugging Face models. To authenticate:

- Get your *Hugging Face API token* from [Hugging Face](https://huggingface.co/settings/tokens).
- Set it in your environment:
  bash
  export HUGGING_FACE_HUB_TOKEN="your_token_here"
  

## Running the Transcription and Analysis Pipeline

### 1. Set Input and Output Paths

Modify the paths in updated-transcription.ipynb to specify:

- *Input video file* (for audio extraction)

Example:

python
input_video_path = "path/to/your/video/*.mp4"


### 2. Execute updated-transcription.ipynb

- Open the notebook and run the cells sequentially.
- This will:
  - Extract audio from the video.
  - Perform speech-to-text transcription.
  - Identify speakers.
  - Analyze sentiment.
  - Apply named entity recognition.

### 3. Run Visualization (updated-visualization.ipynb)

- Ensure transcriptions_with_ner_and_sentiment.csv is generated.
- Open and execute updated-visualization.ipynb to generate graphs.

## Visualization Outputs

1. *Word Count Histogram per 5-Second Bucket*

   - Type: Bar Plot
   - X-Axis: Time Intervals (seconds)
   - Y-Axis: Number of Words Spoken
   - Insight: Identifies active and silent periods in the conversation.

2. *Sentiment Distribution*

   - Type: Bar Plot
   - X-Axis: Sentiment Categories (Positive, Neutral, Negative)
   - Y-Axis: Count of Segments
   - Insight: Displays the overall sentiment balance in the interaction.

3. *Word Count per Speaker*

   - Type: Bar Plot
   - X-Axis: Speaker Labels (e.g., Speaker 1, Speaker 2, etc.)
   - Y-Axis: Number of Words Spoken by each speaker.
   - Insight: Shows how much each speaker contributed.

4. *Word Count Distribution*

   - Type: Bar Plot
   - X-Axis: Word count per segment
   - Y-Axis: Frequency of transcription segments with the corresponding word count
   - Insight: Dsistribution of word counts across all transcription segments, indicating the length of each segment.

5. *Sentiment Trends Over Time*

   - Type: Line Plot
   - X-Axis: Time (seconds)
   - Y-Axis: Average Sentiment Score
   - Insight: Tracks emotional shifts throughout the conversation.

6. *Word Cloud*
   - Type: Word Cloud
   - Insight: Highlights frequently used words for quick topic analysis.

## Contribution Guidelines

If you'd like to improve this tool, fork the repository and submit a pull request. Issues and suggestions are welcome.
No instructions on how to run programs (particularly that file paths would need to be
changed)
Still worked, just missing that element from instructions
