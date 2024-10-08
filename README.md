# Sentiment Analysis On Vietnamese Online Customer Reviews Using Neural Network
## Introduction
The data used are reviews of the Momo e-wallet application scraped from Google Play from April 08, 2023 to May 04, 2024. In the processing stage, the review 
texts will be preprocessed with several requirements. To preprocess Vietnamese data, the research uses the VnCoreNLP tool to separate words, parse, identify entities, and perform tokenization. Then the dataset is labeled ‘positive’ for reviews more than 3 stars, and ‘negative’ for reviews less than 3 stars. To avoid interfering with sentiment analysis results, 3-star reviews will be removed. 

Before being trained, text data needs to be converted into numerical format so the computer can understand it. This technique is called word representation, which can be done by using the BERT tokenizer from the pre-trained BERT-Base Multilingual Cased provided by Google in the Transformers library. After encoding the text, the data will be fed into BERT embedding neural network model architectures to train and predict sentiment. Finally, to evaluate the model, use libraries such as Seaborn, Sklearn and Mathplotlib to calculate metrics such as accuracy, precision, F1 and recall.

## Descriptive Analysis
**The number of reviews**
The dataset of 19,900 Google Play reviews for the Momo eWallet app from April 08, 2023, to May 04, 2024, shows a polarized distribution of ratings. The highest (5 stars) and lowest (1 star) ratings dominate, with 8,816 and 8,804 occurrences, respectively, indicating strong user opinions. In contrast, ratings of 2, 3, and 4 stars are much less frequent, with 718, 718, and 844 occurrences. This suggests that most users either highly praise or strongly criticize the app, while fewer users fall in the middle, expressing neutral opinions.

<img width="426" alt="image" src="https://github.com/user-attachments/assets/459baa96-c221-403a-9fa2-ddc372077acc">

Over the past year, Momo eWallet saw a trend of predominantly negative reviews, particularly between Q2 and early Q4 of 2023, peaking in October with almost 2,000 negative reviews compared to fewer than 1,000 positive ones. However, after October, there was a marked improvement, likely due to Momo's efforts to enhance its brand and service, leading to a surge in positive reviews by early November (around 1,500 positive vs. fewer than 1,000 negative). Despite a dip in Q1 of 2024, where negative reviews again outnumbered positive ones, April 2024 saw a record high of over 2,500 positive reviews, with only around 500 negative ones. This cyclical pattern highlights the dynamic nature of user sentiment and the importance of Momo's ongoing efforts to sustain customer satisfaction.

<img width="444" alt="image" src="https://github.com/user-attachments/assets/035e4a5d-2de1-4aa5-85b2-dca1aa790f4d">

**Positive reviews**

In positive reviews, common words like "tuyệt_vời" (excellent), "tiện_lợi" (convenient), “bảo_mật” (security), and “hài lòng” (satisfied) reflect users' praise for the app's features and benefits. These insights provide valuable information for businesses to enhance product development, marketing, and customer engagement. Additionally, the frequency of positive words surged in October, November 2023, and peaked in April 2024, with words like "ok," "tốt" (good), "tiện_lợi" (convenient), and "nhanh" (fast) being prevalent. This aligns with the analysis of fluctuations in positive reviews.

<img width="423" alt="image" src="https://github.com/user-attachments/assets/e9695f30-4908-4709-8035-c01f25b9c629">

<img width="441" alt="image" src="https://github.com/user-attachments/assets/85d80b43-6ed1-45c1-afa5-882dee75787b">

**Negative reviews**

For the most frequent words in negative reviews, words like "thanh_toán" (payment), "rút_tiền" (withdrawal), "chuyển" (transfer), and "ngân_hàng" (bank) frequently appear, indicating specific issues with transaction processes, fund transfers, and interactions with banks. These negative reviews offer valuable feedback, pinpointing pain points that require urgent attention to improve user satisfaction. Addressing these recurring problems can help Momo enhance the user experience, reduce negative feedback, and potentially increase customer retention.

<img width="424" alt="image" src="https://github.com/user-attachments/assets/4b106b89-136a-482f-8e3d-ed659721fb43">

<img width="436" alt="image" src="https://github.com/user-attachments/assets/a7cf6241-33e6-4458-99d7-fb3774d616f4">

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
