# Sentiment-analysis-on-Twitter-data

1)We loaded all the libraries and also the sentiment.csv file and drop the fields that we don’t need

2)we preprocessed the data to remove links, usernames, or stopwords that could mess up the predictions in the model as they don’t have a contextual meaning in the tweet.

3)We divided 70% of the total data for training and 30% for testing.

4)The data is labeled with positive and negative's. So, in order to keep a common binary classification model, we need to use a label encoder to transform the labels into 0 for negative and 1 for positive.

5)Next step is to tokenize our data, By this point, the tweets are still normal sentences with punctuation, and the tokenization process changes that sequence of characters into tokens. This means, “chopping” the sentences into pieces and throwing away characters as punctuation.

6)LSTM model needs inputs of the same length, a pad function is used to ensure the same length in all the input texts. In this case, the maximum length from the training dataset is taken to pad all the text sequences, both in training and test datasets

7)Created a Sequential model with Embedding, Dropout, LSTM, and Dense layers. First of all, we need to create our embedding layer, which turns the input sequences (cleaned tweets) into dense vectors. To configure this layer, we need values that we’ve already calculated. The vocabulary size is the value taken from the tokenizer vocabulary, the embedding dimension.

8)we’ll train our model for 1 epoch with a batch size of 32. It also uses Adam as an optimization algorithm, categorical_crossentropy as loss function, and accuracy to measure the performance of the model we got accuracy of 84%.

9)We save the model and loaded the model again and predicted the tweet.
