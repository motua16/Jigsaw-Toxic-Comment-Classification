# Jigsaw-Toxic-Comment-Classification

Trained RoBERTa model and Bidirectional LSTM to detect different types of toxicity like `threats, obscenity, insults, and identity-based` in any given sentence. The dataset is of comments from Wikipedia’s talk page edits. Such a model will help online discussion become more productive and respectful, and help authorities to take action against those who write such comments.

This was a kaggle competition hosted in 2018 and the Dataset can be found [here](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/data).
## About

### Project Overview

During conversing on online platforms, discussing things we care about can be difficult sometimes. There is always a threat of abuse and harassment online which means that many people stop expressing themselves and give up on seeking different opinions. Almost all Platforms struggle to effectively facilitate conversations, leading many communities to limit or completely shut down user comments.

In an effort to monitor online conversations, one area of focus is the study of negative online behaviors, like toxic comments (i.e. comments that are rude, disrespectful or otherwise likely to make someone leave a discussion.

The following tasks should be completed 
to create the model:

* Cleaning and preprocessing the Data
* Converting the Data into Datasets and Dataloaders
* Defining the model, training it and make predictions


### Input Data

Dataset consists of comments on Wikipedia Page. Two files are provided.

* train.csv – labelled training data with around 1.5 Lakh sentences

* test.csv – test data with around 1.5 Lakh sentences on which our model will make predictions.

Training Data has the following schema :


|#| Column | Type | Description |
| --- | --- | --- | --- |
| 1 | id | string | Unique identifier of a comment|
| 2 | comment_text | string | comment |
| 3 | toxic | int | 0 or 1 to signify if the comment is toxic or not |
| 4 | severe_toxic | int | 0 or 1 to signify if the comment is severely toxic or not |
| 5 | obscene | int | 0 or 1 to signify if the comment is obscene or not |
| 6 | threat | int | 0 or 1 to signify if the comment is threatening in nature or not |
| 7 | insult | int |0 or 1 to signify if the comment is insulting in nature or not |
| 8 | identity_hate | int |0 or 1 to signify if the comment propagates hate |

## Repository Structure

```
- dir
| - processed-data
| |- clean-train.csv # cleaned training data
| |- clean-test.csv # cleaned test data
|- README.md
|- model-bert.ipynb # notebook with RoBERTa model 
|- model-bilstm.ipynb # notebook with Bidirectional LSTM model
|- submission.csv # sample submission on kaggle

```

## Conclusion & Improvement

I tried training with two models RoBERTa and Bi-LSTM. RoBERTa performed better as expected. 


Some improvements that can be made are :

* not all comments are in proper english, people use raw english in usage, devising a strategy to effectively convert words to meaningful english will surely improve the performance
* Trying other models such as XLNet, and other embeddings such as ELMo etc
* Adapting this model to all commonnly used languages along with english


