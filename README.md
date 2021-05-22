# roBERTsaikwan-model
Model for RoBERTSaiKwan News Summarizer (Extractive).

## Fine-tuning
This model use wangchanBERTaQA as a BERT and then fine-tune with the data from thaisum. Since we use model qa as a base we need to create new label for our model. The algorithm called oracle-b find a range of words maximizes the rouge score. It helps generate the label to be trained in the model. The code for fine-tuning the model is [here](https://github.com/Sav-eng/roBERTsaikwan-model/blob/main/fine_tuning_roBERTsaikwan.ipynb). You can simply fine-tune the new data by following the guideline in the notebook. Note that you should read through each sections as it need to set the data(preprocess)

## Inference
The part uses model which is already fine-tined to inference.

## Metrics
Our code are in [Metrics.ipyn](https://github.com/Sav-eng/roBERTsaikwan-model/blob/main/Metrics.ipynb).
We use 3 model to compare with our model: Lead-3 (simply three sentences at the beginning, oracle-a(selected words to maximize rouge score), and oracle-b which is our gold label)

## Resources
Some of the data such as preprocessed data are too big to be pushed to github, therefore here is all the link you can download.

### Preprocess Data
You can download our preprocessed data by loading from google drive or loading in code.

[Train dataset](https://drive.google.com/file/d/1-3RreaZi4soUuHD414nkNfCK_uwQooRf/view) is the dataset for fine-tuning the model. 

[Validation_true.json](https://drive.google.com/file/d/1_zJds0bj7uXh0h-T2a9kPiT9XxkgtSfX/view) is the dataset for validate the model when fine-tining.

[Test_true.json](https://drive.google.com/file/d/1-298pxpI2JDPbhQhtCeaw52QBqjHdJNh/view) is the dataset for testing the model.

### Model
[Here](https://drive.google.com/file/d/1sEWiK5ZiRVJYDI8F-hFKkIM7-CAjbDUe/view) is the model that already fine-tuned.

## Note
Note that the web-application are in the other repositories in both [fronend](https://github.com/rew150/robertsaikwan_frontend) and [backend](https://github.com/rew150/robertsaikwan_backend)
