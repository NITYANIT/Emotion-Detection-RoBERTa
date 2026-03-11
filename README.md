Emotion Shift Detection using RoBERTa

Emotion detection and emotion flow analysis in text using a pretrained RoBERTa model.

Project Overview

Emotion detection is a Natural Language Processing task that identifies emotions expressed in text.

This project detects emotions in each sentence of a paragraph and shows how the emotion changes across the text (emotion flow).

The system uses a pretrained RoBERTa transformer model trained on the GoEmotions dataset.

Example
Input
I was excited about the trip.
Later the weather became terrible and I felt sad.
Finally we enjoyed the evening again.
Output
Sentence Emotions

I was excited about the trip → Joy
Later the weather became terrible and I felt sad → Sadness
Finally we enjoyed the evening again → Joy

Emotion Flow
Joy → Sadness → Joy
Model Used

Model: roberta-base-go_emotions

The RoBERTa model is a transformer-based NLP model that improves upon BERT by using:

More training data

Dynamic masking

Larger batch training

The model is pretrained and fine-tuned for emotion classification.

Dataset

Dataset used: GoEmotions

Features:

Created by Google Research

~58,000 Reddit comments

27 emotion categories

Example emotion labels:

Joy

Sadness

Anger

Surprise

Fear

Disappointment

Gratitude

Model Architecture

Pipeline used in the project:

Input Paragraph
        ↓
Sentence Tokenization (NLTK)
        ↓
RoBERTa Tokenizer
        ↓
Token IDs
        ↓
Embedding Layer
        ↓
Transformer Layers (Self-Attention)
        ↓
Classification Layer
        ↓
Emotion Prediction

Each sentence is processed independently to determine the most probable emotion.

Performance

Evaluation metric: Macro F1 Score

Reported results on the GoEmotions dataset:

Model	Macro F1 Score
BERT	0.46
RoBERTa	~0.50

RoBERTa improves performance by better contextual understanding.

Technologies Used

Python

PyTorch

Hugging Face Transformers

NLTK

Google Colab

How to Run

Install required libraries:

pip install transformers torch nltk

Run the notebook or Python script and provide a paragraph as input.

The model will output:

Emotion for each sentence

Emotion flow across sentences

Limitations

Maximum context length is 512 tokens

Emotion detection may struggle with sarcasm or implicit emotions

Repository Structure
Emotion-Detection-RoBERTa
│
├── emotion_detection.ipynb
├── README.md
└── screenshots

You can add screenshots of model output inside the screenshots folder.

References

GoEmotions Dataset Paper
https://arxiv.org/abs/2005.00547

RoBERTa GoEmotions Model
https://huggingface.co/SamLowe/roberta-base-go_emotions

Evaluation Notebook
https://github.com/samlowe/go_emotions-dataset
