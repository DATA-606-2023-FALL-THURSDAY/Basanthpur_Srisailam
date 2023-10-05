# Title and Author

- **Project Title**: Text Classifier using CNN
- **Prepared for UMBC Data Science Master Degree Capstone by**: Dr. Chaojie (Jay) Wang
- **Author**: Srisailam Basanthpur
- **Link to the author's GitHub profile**: [GitHub Profile](https://github.com/sribasanth123)
- **Link to the author's LinkedIn profile**: [LinkedIn Profile](https://www.linkedin.com/in/srisailam-basanthpur-687390184/)

# Background

So far, Convolution Neural Networks (CNN) are usually used for image processing. In this study, we aim to analyze if CNN can also be used for processing text.

# Research Question

Convolution Neural Networks are usually used for image processing. So, for this study, we want to investigate whether CNN can be effectively applied to text processing.

# Data

- The data is provided in the form of text files and does not contain any tabular format data.
- The dataset consists of approximately 20,000 newsgroup documents from 20 different newsgroups, with a total size of approximately 46 MB.
- Source: [Dataset Source](https://archive.ics.uci.edu/dataset/113/twenty+newsgroups)
- Data Size: 46MB
- Data Shape (Number of Rows and Columns): It does not follow a traditional tabular structure; instead, data is present in the form of text files (.txt format).
- The data represents different news articles.
- Text documents serve as the input variables, and the target variables are the class labels (Name of the class group).

## Progress as of 6th Oct 2023

1. There are 19,997 documents in the dataset in the form of text files. These documents are grouped into 20 newsgroups. They are:

   - alt.atheism
   - comp.graphics
   - comp.os.ms-windows.misc
   - comp.sys.ibm.pc.hardware
   - comp.sys.mac.hardware
   - comp.windows.x
   - misc.forsale
   - rec.autos
   - rec.motorcycles
   - rec.sport.baseball
   - rec.sport.hockey
   - sci.crypt
   - sci.electronics
   - sci.med
   - sci.space
   - soc.religion.christian
   - talk.politics.guns
   - talk.politics.mideast
   - talk.politics.misc
   - talk.religion.misc

2. The data is distributed almost equally among all the newsgroups.

3. The data is then cleaned using python regular expressions.

4. As part of cleaning, 3 functions have been created.

5. The first function is email processing which takes text as the input in string format and processes the words with email extensions and returns a string which is concatenated with a list of such words.

6. The second function is subject processing which takes text as the input and processes the text line after the word “Subject” and returns the string.

7. The third function is text processing which takes text as the input and performs a series of operations to remove all the unwanted characters and returns the string.

8. These functions are then applied to the documents, and outputs are stored in separate lists.

9. The data frame is created with the above lists and then stored in a pickle file.

10. The email, subject, and text data are concatenated and stored into a single variable as a dependent variable.

11. All the target labels are stored in an independent variable.

12. The data is then split into train and test in the ratio of 75%:25%.

13. The target labels are encoded using label encoder and are then converted to one-hot encoded representation.

14. The train and test datasets are vectorized using Tokenizer and are then padded.

15. Glove vectors of 100 dimensions have been used.

16. An embedding matrix is formed for all the words in the Tokenizer using glove vectors.

17. The model is then built using TensorFlow.
