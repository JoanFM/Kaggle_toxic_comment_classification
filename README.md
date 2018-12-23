# Kaggle_toxic_comment_classification
Solution proposal for the Kaggle competition for Toxic Comment classification

This proposal is based on 3 key ingredients:
- Word2Vec embedding
- Extra features
- CNN

# Word2Vec embedding
The comments are padded to a max_length of 200 words and the word2vec pretrained embedding trained on Google News is used to have an embedding to a 300 dimension space.
With this we avoid having such sparse vectors and we can gain context and semantic deeper information from words.

# Extra features
Extra handmade features are included in the model that can potentially help in the classification task. These features include the number of exclamation marks, the number of capital letters used, etc...

# Convolutional Neural Network
Although an NLP problem like this one is usally tackled using RNN, in this case, and given the classification nature of the task a 1 dimensional Convolution Network can do the work.
In this case we do not need to remember things from the beginning of the sentence but it is interesting have some 'locality' of the features which is obtained using the stack of conv layers.


