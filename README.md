# Fake News Detection with BERT :newspaper:

This model uses TL to build upon the pretrained model BERT to classify news articles into either fake or real news. 

1. First, download all the files from the repository.
2. Ensure that you install the **Kaggle API** by running the following command:
   ```bash
   !pip install kaggle
   ```
3. Download the dataset from Kaggle:
   ```bash
   !kaggle datasets download -d emineyetm/fake-news-detection-datasets
   ```
4. After downloading the dataset, you should be able to extract it and load it into your Python environment.
5. If available, run on a GPU for faster training. If you're using Google Colab, make sure to select GPU from the runtime settings.
6. Train and Evaluate model within the given code. Model achieves 99% accuracy. Further metrics below: \n
               precision    recall  f1-score   support
           
           0       1.00      0.99      0.99     23481
           1       0.98      1.00      0.99     21417

## External Libraries Used:
This project was developed using **PyTorch** for deep learning, with the **Hugging Face Transformers** library for pretrained BERT models. The **scikit-learn** library was used for preprocessing, and **numpy** and **pandas** helped with data manipulation and handling. The model utilizes **CrossEntropyLoss** for classification and **AdamW** optimizer for fine-tuning the BERT model.

Key libraries:
- **PyTorch**: Deep learning framework.
- **Hugging Face Transformers**: Used to load the pretrained BERT model.
- **scikit-learn**: For data preprocessing and model evaluation.
  
## :shipit:
