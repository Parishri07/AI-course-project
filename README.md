# AI-Project-

## Project Overview

This project, Emotion Recognition and Contextual Summarization for Mental Health Conversations, aims to provide AI-driven mental health assistance by recognizing emotions in conversations and summarizing contextually relevant content. We implemented two distinct approaches to achieve robust emotion detection and contextual understanding: **Audio-Driven Emotion Recognition (ADER)** and **Contextual Summarization and Emotion Prediction (CSEP)**.

## Team Members
1. Ravi Raj - 22bds051
2. Parishri Shah - 22bds043
3. Pakhi Singhal - 22bds042
4. Preethi Varshala S - 22bds045


## Methodology

1. **Method 1**: The **ADER approach** leverages audio analysis for emotion prediction. The process begins by converting text into audio using the Google Text-to-Speech (GTTS) system. This ensures that emotion recognition can incorporate speech characteristics for a richer understanding of emotional tones.  Key audio features are extracted using Mel-frequency cepstral coefficients (MFCC), which capture essential sound patterns relevant to human speech. These features are then utilized as inputs for machine learning models. We trained **XGBoost** and **Random Forest** classifiers on these extracted features to predict emotional states. The system can generalize effectively, providing accurate emotion predictions on unseen audio inputs, enhancing its utility in diverse conversational scenarios.

![Flow diagram](images/flowchart-2.jpg)

2. **Method 2**: The **CSEP approach** focuses on emotion detection directly from text while summarizing the context for concise insights. Initially, the dataset undergoes preprocessing steps, including **tokenization of utterances** and **label encoding** for the Dialogue Act and Emotion columns. We employed a custom **BERT-based model** for embedding the input data, which was implemented using **PyTorch**. This model learns contextual representations of the conversations, enabling more accurate emotion predictions. Additionally, a **summarization model** using **BART** with a dynamic threshold of 30 is applied to the dataset, providing a condensed version of the conversation while retaining its emotional essence. This helps streamline the analysis and enhances the interpretability of long conversations, ensuring the system delivers high-quality, actionable insights for mental health support.


![Flow diagram](images/flowchart-1.jpg)



## How to run
1. Audio-Driven Emotion Recognition (ADER)<br />
File name : Conversion-to-audio-emotion-detection.ipynb<br />
Dataset Name : 5247-rows_3-Emotions_No-Type.xlsx<br />
Key Steps :<br />
a) Install Dependencies - Install the gTTS library using pip install gTTS<br />
b) Upload the dataset<br />
c) Run the 'Conversion-to-audio-emotion-detection.ipynb' file which converts the text in the 'Utterance' column to audio (.mp3) using gTTS. Then detects emotion of the audio file.<br />
d) Saves audio files in the designated output directory (audio_outputs_gtts).<br />
e) Outputs - Generates audio files corresponding to each utterance.<br />
f) Prediction - Upload .mp3 file then the model predicts the emotion of the speech.<br />

3. Contextual Summarization and Emotion Prediction (CSEP)<br />
File name : Emotions-Detection-Using-Text-Utterance.ipynb<br />
Dataset Name : 5247-rows_3-Emotions_No-Type.xlsx<br />
Key Steps :<br />
a) Install Dependencies - Install Dependencies<br />
b) Upload the dataset<br />
c) Run the 'Emotions-Detection-Using-Text-Utterance.ipynb' file which detects emotion of the text in the Utterance column.<br />
d) Prediction - Upload any text. It summarizes the text if word count is more than 30 and then predicts the emotion.<br />


## Key Contributions

1. **Emotion Recognition through Audio and Text**: ADER integrates audio analysis, while CSEP enhances emotion recognition with contextual textual insights.
2. **Advanced Modeling Techniques**: The use of ML models like XGBoost, Random Forest, and a custom BERT model ensures robust emotion prediction.
3. **Summarization for Better Context**: The summarization model in CSEP enables the system to focus on the most relevant parts of the conversation, improving decision-making and emotional analysis.


## Presentation Slides
[PPT](AI_Project_Presentation.pptx) 

