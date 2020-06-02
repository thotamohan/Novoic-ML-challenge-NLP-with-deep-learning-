# **Spam SMS Filtering System**

## **Introduction:**
This project is done as part of the Novoic Machine Learning challenge, here the task is to classify the given SMS messages as Spam and Ham(legitimate).

## **Dataset Description:**
The data comprises 5,574 SMS messages. Each message is labelled as either 'ham' (legitimate) or spam.

Each line in data.txt corresponds to one message. The first word is the data label (either ham or spam), followed by a tab (\t) character and then the message.

## **Approach:**

Since this is an open-ended challenge, we are welcomed to use our creativity in analyzing data. The project comprises of following activities.
* Binary Classification.
* Data exploration and visualization.
* Unsupervised Clustering.

## **Training and Test Dataset:**

Firstly the label count is checked and it is known that there are a total of 4827 Ham and 747 Spam messages are there in the dataset which is an imbalanced dataset. Therefore in order to split the dataset into training set  and test set stratified train test split method is used as it can help in equal distribution of ham and spam in both the sets.

After applying stratified train-test split, these are the counts in the training and test set:
* Training Set: 3620 Ham and Spam 560
* Test Set: 1207 Ham and 187 Spam 

## **Preprocessing:**

As we are aware that inorder to obtain best classification results, preprocessing of the data is the most important thing in data science tasks, as it helps our model to learn from data and not things which we dont want our model to learn from.

For this task, I performed all preprocessing tasks with related to text data such as removing punctuation, removing of single digit and numeric, tokenized each message and the removal of all the stopwords in english as all the messages are english, and all the words are stemmatized and lemmatized.

## **Binary Classification:**

Here inorder to perform the binary classification, Bidirectional LSTM layer is used along with maxpool, relu dense layer, dropout  and sigmoid dense layer is used in the end.

In this model, binary cross-entropy loss is used and adam-optimizer is used to find minima and accuracy is used as metric.

## **Results:**
After performing the classification task, the results are as follows
* **F1 score of 95.55% is obtained.**
* **precision and recall of 99.42% and 91.98% respectively.**
* The confusion matrix is also displayed.

![Image of Sensorplacement](https://github.com/thotamohan/Novoic-ML-challenge-NLP-with-deep-learning-/blob/master/SMS-confusion.png)


## **Unsupervised Clustering:**

Using term frequency and inverse document frequency, text is analyzed in order to find the top key words in the messages.
The top keywords are as follows:

|features |    score|
|-----|-----|
|im | 0.020115|
|ok | 0.019064|
|come|0.015771|
|ill|0.014245|
|ur|0.013168|
|ltgt|0.012627|
|dont|0.012480|
|know|0.012359|
|time |0.012096|
|good |0.011865|

## **K-means Clustering:**

In addition to the deep learning model, K-means clustering is also performed for the classification of spam and ham messages. After performing the clustering, the top keywords as per tf-idf in both the tasks are visualized.

![Image of Sensorplacement](https://github.com/thotamohan/Novoic-ML-challenge-NLP-with-deep-learning-/blob/master/clustering-results.png)

Here the cluster 0 represents Ham and the cluster 1 represents spam.

From the above figure we could see that spam messages mostly consists of words like **prize, cash, free,claim,award** etc..

Then going further using this important spam keywords we can further group messages based on the keyword

Where as in the case of ham messages, the top words present are **ok, im, home,come** which are used in day-day activities







