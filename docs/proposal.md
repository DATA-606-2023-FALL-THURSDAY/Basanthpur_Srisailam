## Objective
The main objective of this project is to build a text classifier using CNN which takes text as the input and predicts the label.

## Dataset details
The dataset contains 18,000(Approx) newsgroup documents from 20 different newsgroups. The dataset is of size 46 MB approximately.

[Source](https://www.kaggle.com/datasets/crawford/20-newsgroups?resource=download)

## Research Question
Convolution Neural Networks are usually used for image processing. So, for this study I am going to analyze if it can also be used for processing text.

## Approach
- The text documents are first cleaned and processed using python regex which involves removing punctuations, converting non-English words to English etc.,
- The cleaned text documents are then vectorized.
- We use pre-trained glove vectors for vectorizing the text.
- CNN architectures are built and are trained using the above vectorized documents.
- Results are evaluated for the train, test datasets.
  
