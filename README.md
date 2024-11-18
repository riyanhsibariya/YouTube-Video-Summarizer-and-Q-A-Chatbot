# YouTube Video Summarizer and Q&A Chatbot  

This project is an interactive tool designed to extract, summarize, and provide Q&A capabilities for YouTube video content. It uses **state-of-the-art NLP models** to process video transcripts and offers a user-friendly interface via **Gradio**, making it ideal for educational and research purposes.  

---

## Table of Contents  
- [Features](#features)  
- [Technologies Used](#technologies-used)  
- [Setup and Usage](#setup-and-usage)  
- [How It Works](#how-it-works)  
- [File Structure](#file-structure)  
- [License](#license)  

---

## Features  

1. **Summarization**:  
   - Extracts transcripts from YouTube videos.  
   - Summarizes video content into concise, easy-to-read text.  

2. **Q&A Capability**:  
   - Ask questions about the summarized content and get context-aware answers.  

3. **Interactive Interface**:  
   - A **Gradio-based UI** for seamless interaction and exploration.  

---

## Technologies Used  

### Libraries  
- **Gradio**: For building the interactive user interface.  
- **YouTube Transcript API**: To fetch video transcripts directly from YouTube.  
- **Transformers**: For utilizing pre-trained NLP models:  
  - `facebook/bart-large-cnn` for summarization.  
  - `bert-large-uncased-whole-word-masking-finetuned-squad` for Q&A.  

### Models  
- **BART**: A Transformer-based architecture specialized in summarization tasks.  
- **BERT**: A state-of-the-art NLP model fine-tuned for Q&A using the SQuAD dataset.  

---

## Setup and Usage  

This project is designed to be run on **Google Colab** for ease of setup and access to GPU resources. Follow the steps below:  

### Steps  

1. **Open Google Colab**:  
   - Go to [Google Colab](https://colab.research.google.com/).  

2. **Upload the Script**:  
   - Upload the `app.py` file to your Colab environment.  

3. **Install Dependencies**:  
   Run the following command to install the required libraries:  
   ```python  
   !pip install gradio youtube-transcript-api transformers  
