# FakevsReal_News 
Supervised machine learning project on news to predict weither they are Real or Fake news.

### Description
The complete dataset is from Kaggle (https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset). It is initially 2 datasets, one for the true news, the other one for the fake news. Each dataset is a collection of about 22000 news, exactly 44898 datas in total before cleaning. It stores : the title of the article, the complete text of the article, its data, and its subject.

##### Cleaning 

###### General cleaning of the dataset :
- Removal of empty rows and of 209 duplicated rows. 
- Creation of 7 columns : source of the article, number of characters and special characters in the title, in the text, if the article contains image(s), countries quoted in the article

###### Text cleaning :
- Tokenization / Stemming (nltk library) : to keep only the root meaning of the words (in order to avoid getting two different words with the same meaning, which is useless). Example : "computer", , "computers", "computing" => becomes "comput".

###### Clustering (unsupervised machine learning)
Unsupervised machine learning had been use here to create clusters that stores similar news.
Kmeans from sklearn libraries had pretty good results.

### Objective

This project's objective is to use machine supervised machine learning and try to predict weither a news is real or fake.
The metrics of interest is recall, because the idea is to minize the false positive (a fake news considered as a true news).

### Results

###### Modelling
To reduce overfitting, the dataset had been splitted as following : train / test, and train dataset had been splitted again into train / validation.

Severall models reached 100% accuracy for the train/validation datasets : 
- Logistic regression
- Gaussian Naive Bayes
- Decision trees & random forest
- Ada Boost

The results of these particular models were the same for the testing (train/test).

###### Features importance

The 2 most important features used to determine if a news is true or fake are : 
- the source
- the subject



