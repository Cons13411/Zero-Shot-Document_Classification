This is the code to perform zero-shot cross-lingual document classification. 
(However, it is also can be used for supervised document classification)

It is implemented using Pytorch. The model is a fully connected feed forward network, that at time that you want build it, you have the option to modify
every part of it, from the number of layers to the activation function of each layer and dropout. 

The model gets as input, word embeddings so it can produce document representations, and also the train-validation-test set of MLDoc data set, which you can
download from this [link.](https://github.com/facebookresearch/MLDoc)

To form the document embeddings, I use the average embeddings, instead of weighted average since I did not want to assign a large weight to the very rare words.

For the zero-shot classification, you just need to pass the train and validation for your source language and its cross-lingual embeddings, and then testing
the trained model on the target language using its cross-lingual embeddings, which are in the same vector space as the source language embeddings. 


