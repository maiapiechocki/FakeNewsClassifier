Maia Piechocki
piechock@usc.edu

Introduction: 

This model uses TL to build upon the pretrained model BERT to classify news articles into either fake or real news.

1. Dataset & Preprocessing: 

Preprocessing included tokenizing the text using BERT’s tokenizer, padding/truncating sequences to a fixed length, and using an attention mask to handle padding. These steps ensure the model can process varying text lengths and focus only on meaningful tokens.

2. Model Development and Trianing:

I implemented a custom BERT architecture, using BERT as the core model due to its strong pre-trained language understanding. I made modifications by freezing the layers of the BERT model, allowing the model to retain the pre-trained knowledge. After extracting the [CLS] token's representation from BERT, I passed it through a custom fully connected layer (512 neurons), followed by a ReLU activation to introduce non-linearity and a dropout layer for regularization to prevent overfitting. This output was then passed through a second fully connected layer to produce the class scores.
The model was trained using the AdamW optimizer and CrossEntropyLoss for binary classification. The learning rate was set to 1e-5, and the batch size was set to 32. The model was trained for 1 epoch. These choices were made after fine-tuning the model's parameters, aiming to maximize training and validation accuracy while accounting for the relatively small dataset size.

3. Model Evaluation/Results:

Model evaluation was done using accuracy and loss, with a final validation accuracy of 99% and a validation loss of 0.027. Recall was .99 for fake news and 1.0 for real news. f1-score for fake news was .99 for both fake and real news.

4. Discussion:
The dataset, model architecture, and training procedures fit well for the task of fake news detection. BERT provides strong pre-trained language understanding, coupled with custom layers trained to the dataset, producing a very accurate model.

This work can contribute to social good by automating fake news detection and aiding in the fight against misinformation. However, the model’s generalization capability might be limited by the dataset size and the binary nature of the classification. 

References that helped me understand BERT structure include:
- BERT tutorial implementation: 
https://www.kaggle.com/code/harshjain123/bert-for-everyone-tutorial-implementation
- BERT architecture: https://stackoverflow.com/questions/77164276/bert-arch-has-no-attribute-predict-error-while-loading-pretrained-model-in-gradi 

5. Next Steps:
To improve the model, I would expand the dataset to include more diverse sources of news, ensuring that it generalizes well to a broader range of content. Additionally, I would implement functionality to save the best model weights during training to avoid losing the best-performing version. Since running the model on a CPU was very time-consuming, I would optimize the training and evaluation process by utilizing parallel computing through data loaders and workers, ensuring faster computation when GPU usage is not available(ran into colab GPU limits). Further, using a more diverse training set and adding a multi-class classification model that could classify news as politics, celebrity drama, or other categories could enhance its utility. Last, incorporating more advanced techniques like adversarial training could also strengthen the model's robustness and help it handle more challenging, real-world data.

