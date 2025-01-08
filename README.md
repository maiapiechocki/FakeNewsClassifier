# Fake News Detection with BERT :newspaper:


1. First, download all the files from the repository.
2. Install the **Kaggle API** by running the following command:
   ```bash
   !pip install kaggle
   ```
3. Download the dataset from Kaggle:
   ```bash
   !kaggle datasets download -d emineyetm/fake-news-detection-datasets
   ```
4. After downloading the dataset, extract it and load it into your Python environment.
5. Ensure you're running on a GPU for faster training. If you're using Google Colab, make sure to select GPU from the runtime settings.
6. Train and evaluate the model internally.

## External Libraries Used:
This project was developed using **PyTorch** for deep learning, with the **Hugging Face Transformers** library for pretrained BERT models. The **scikit-learn** library was used for preprocessing, and **numpy** and **pandas** helped with data manipulation and handling. The model utilizes **CrossEntropyLoss** for classification and **AdamW** optimizer for fine-tuning the BERT model.

Key libraries:
- **PyTorch**: Deep learning framework.
- **Hugging Face Transformers**: Used to load the pretrained BERT model.
- **scikit-learn**: For data preprocessing and model evaluation.
  
## :shipit:
