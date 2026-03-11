"KINDLY DOWNLOAD AND OPEN THROUGH VSCODE TO VIEW THE 'emotionshiftdetector.ipynb' file. "




Emotion Shift Detection using RoBERTa

This project detects emotions in text and shows how emotions change across sentences in a paragraph. The model used is roberta-base-go_emotions, a pretrained RoBERTa model trained on the GoEmotions dataset.

Example

Input:
I was excited about the trip. Then the weather became terrible. I felt disappointed.

Output:
I was excited about the trip → Joy
Then the weather became terrible → Sadness
I felt disappointed → Disappointment

Emotion Flow:
Joy → Sadness → Disappointment

Model used
roberta-base-go_emotions

Dataset
GoEmotions dataset created by Google Research
Around 58,000 Reddit comments with 27 emotion labels.

Tools used
Python
PyTorch
Hugging Face Transformers
NLTK
Google Colab

Performance
Metric: Macro F1 Score
RoBERTa performance on GoEmotions dataset: ~0.50

References

https://huggingface.co/SamLowe/roberta-base-go_emotions

https://github.com/samlowe/go_emotions-dataset

https://arxiv.org/abs/2005.00547
