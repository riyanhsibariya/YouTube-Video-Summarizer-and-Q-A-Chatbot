# YouTube Video Summarizer and Q&A Chatbot  

This project is an AI-powered chatbot designed to process YouTube videos, generate detailed summaries, and enable users to interactively ask questions about the content. It utilizes advanced Natural Language Processing (NLP) models and libraries to deliver concise and informative outputs. Running entirely in Google Colab, this project ensures accessibility and easy usage without requiring extensive local setup. 

---

## Table of Contents  
- [Features](#features)  
- [Technologies Used](#technologies-used)  
- [Setup and Usage](#setup-and-usage)  
- [How It Works](#how-it-works)  


---

## Features  


1. **YouTube Video Processing**  
   - Extracts transcripts using the **YouTube Transcript API** for videos with captions.  
   - Processes and organizes the transcript into coherent text for summarization.  

2. **Detailed Summarization**  
   - Utilizes the **BART model (facebook/bart-large-cnn)** for summarizing lengthy transcripts into multi-line summaries.  
   - **BART (Bidirectional and Auto-Regressive Transformers)** is a transformer-based encoder-decoder model, fine-tuned specifically for summarization tasks.  

3. **Question Answering (Q&A)**  
   - Employs the **DistilBERT model (distilbert-base-cased-distilled-squad)** to understand user questions and generate accurate responses based on the summarized content.  
   - **DistilBERT is a smaller, faster version of BERT (Bidirectional Encoder Representations from Transformers)** trained on the SQuAD dataset for question-answering tasks.  

4. **Interactive User Interface**  
   - Built using **Gradio**, a Python library for creating web-based UIs directly from scripts.  
   - The interface allows users to input a YouTube URL, view the summary, and ask questions seamlessly.  

---

## Technologies Used  

### 1. **Natural Language Processing Models**  
- **BART (facebook/bart-large-cnn)**  
  - A pre-trained transformer model for abstractive text summarization.  
  - Fine-tuned to handle long inputs and generate coherent, concise summaries.  

- **DistilBERT (distilbert-base-cased-distilled-squad)**  
  - A lightweight version of BERT, optimized for efficiency while retaining high accuracy.  
  - Fine-tuned for question-answering tasks on **SQuAD** (Stanford Question Answering Dataset).  

### 2. **YouTube Transcript API**  
- Retrieves subtitles or transcripts from YouTube videos.  
- Automatically extracts text from captions to prepare input for summarization.  

### 3. **Transformers Library**  
- Developed by **Hugging Face**, this library provides access to state-of-the-art NLP models.  
- Enables easy integration of BART and DistilBERT models into Python workflows.  

### 4. **Gradio**  
- Simplifies the creation of an interactive UI for users to input video links, view summaries, and ask questions.  
- Generates shareable web links to the app, making it accessible from any device.  

### 5. **Google Colab**  
- A cloud-based platform that supports running Python scripts with access to GPUs.  
- Eliminates the need for local setup, making the project accessible and efficient.  

---

## Setup and Usage  

This project is designed to be run on **Google Colab** for ease of setup and access to GPU resources. Follow the steps below:  

### Steps  

1. **Open Google Colab**:  
   - Go to [Google Colab](https://colab.research.google.com/).  

2. **Upload the Script**:  
   - Upload the `youtube_chatbot.ipynb` file to your Colab environment. 

3. **Install Dependencies**:  
   Run the following command to install the required libraries:  
   !pip install gradio youtube-transcript-api transformers
   Install the required libraries using the provided code snippets.
   Paste the YouTube video URL into the Gradio app's input field.  
   Wait for the system to extract the transcript and generate a summary.  
   Use the interactive Q&A feature to ask questions about the video content.  
   Share the Gradio app link if needed. 
---

## How It Works  

The application processes YouTube videos and provides summarized content and Q&A capabilities through the following steps:

1. **Transcript Extraction**  
   - The **YouTube Transcript API** retrieves the transcript from the video URL.  
   - Captions are combined into a continuous text format for processing.  

2. **Summarization**  
   - The transcript is passed to the **BART-based summarization model** (`facebook/bart-large-cnn`) from the **Transformers** library.  
   - This model compresses the transcript into a concise, multi-line summary that retains key details.  

3. **Q&A Capability**  
   - The **BERT-based model** (`bert-large-uncased-whole-word-masking-finetuned-squad`) processes questions along with the summary.  
   - The model searches the summary context for the most relevant answer and provides a detailed response.  

4. **Interactive UI**  
   - **Gradio** creates an intuitive and user-friendly interface:  
     - Users input the YouTube video URL.  
     - The application generates a detailed summary.  
     - Users can ask questions based on the video content and get relevant answers.  

This workflow ensures the application is efficient, accurate, and user-friendly, leveraging advanced NLP techniques.
