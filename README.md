# Sentiment Analysis On Vietnamese Online Customer Reviews Using Neural Network
## Introduction
The data used are reviews of the Momo e-wallet application scraped from Google Play from April 08, 2023 to May 04, 2024. In the processing stage, the review 
texts will be preprocessed with several requirements. To preprocess Vietnamese data, the research uses the VnCoreNLP tool to separate words, parse, identify entities, and perform tokenization. Then the dataset is labeled ‘positive’ for reviews more than 3 stars, and ‘negative’ for reviews less than 3 stars. To avoid interfering with sentiment analysis results, 3-star reviews will be removed. 

Before being trained, text data needs to be converted into numerical format so the computer can understand it. This technique is called word representation, which can be done by using the BERT tokenizer from the pre-trained BERT-Base Multilingual Cased provided by Google in the Transformers library. After encoding the text, the data will be fed into BERT embedding neural network model architectures to train and predict sentiment. Finally, to evaluate the model, use libraries such as Seaborn, Sklearn and Mathplotlib to calculate metrics such as accuracy, precision, F1 and recall.

## Model training using neural network architectures
### The BERT-LSTM model

<img width="563" alt="image" src="https://github.com/user-attachments/assets/4d3ab324-1218-43a0-a8a1-6dc38965541b">

### The BERT-TextCNN model

<img width="420" alt="image" src="https://github.com/user-attachments/assets/211d576f-e2dd-4d70-addb-e1cd863b859c">

### The BERT-RCNN model

<img width="333" alt="image" src="https://github.com/user-attachments/assets/61ac89b2-ea9d-4c3a-b4f6-7fc2ea27b177">

## Comparison of model results
Overall, while all three models demonstrate strong performance in sentiment analysis tasks, the BERT-TextCNN model showcases slightly superior performance, particularly in terms of precision and the F1 score. However, the BERT-LSTM model also performs admirably well, especially in terms of recall. The choice of model may ultimately depend on specific requirements and priorities for the sentiment analysis task at hand, such as the importance of precision, recall, or overall balance between the two.

<img width="552" alt="image" src="https://github.com/user-attachments/assets/c2c006dd-eea9-4990-9f43-31832ab18b9a">

