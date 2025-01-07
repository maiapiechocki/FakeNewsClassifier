# Fake News Detection with BERT :newspaper:

## Created By: Maia Piechocki

## How to Compile/Execute :computer:

1. First, download all the files from the repository.
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Download the dataset or load your own dataset.
4. Train the model by running the following command:
   ```bash
   python train.py
   ```
5. After training, you can evaluate the model using:
   ```bash
   python evaluate.py
   ```
6. The trained model will be saved, and you can use it for inference on new text data.

## External Libraries Used:
This project was developed using **PyTorch** for deep learning, with the **Hugging Face Transformers** library for pretrained BERT models. The **scikit-learn** library was used for preprocessing, and **numpy** and **pandas** helped with data manipulation and handling. The model utilizes **CrossEntropyLoss** for classification and **AdamW** optimizer for fine-tuning the BERT model.

Key libraries:
- **PyTorch**: Deep learning framework.
- **Hugging Face Transformers**: Used to load the pretrained BERT model.
- **scikit-learn**: For data preprocessing and model evaluation.

### :shipit:
