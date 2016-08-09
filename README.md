## Capstone

Analyzing and Predicting ISIS Tweets 

In this project, I am analyzing tweets from ISIS fan boys on Twitter. I used visualization tools and Machine Learning to study my dataset.

## 1- The Dataset:

 • Scraped over 17,000 tweets from 100+ pro ISIS users.
 
 • Period: November 2015 (Paris Attack) to May 2016.
 
 • Owner: Fifth Tribe LLC.
 
 • Source: Kaggle datasets “How ISIS Uses Twitter” 


## 2- The task:

How to analyze the tweets and derive insights from them.

## 3- EDA:
•Tableau : I mostly used Tableau Software to get some instincts of the data: Most followed user name, User name with most tweets, days with most tweets...etc

## Some useful insights

## Tweets timeline
![alt tag](https://github.com/Redwa/Capstone/blob/master/img/TweetstrendMonth.png)

## Most followed user
![alt tag](https://github.com/Redwa/Capstone/blob/master/img/Most%20Followed.png)

## Most tweets by user and Location:

![alt tag](https://github.com/Redwa/Capstone/blob/master/img/tweetsbyUsername.png)

## Tweets by day

![alt tag](https://github.com/Redwa/Capstone/blob/master/img/Tweetsbyday.png)

## Most used words
![alt tag](https://github.com/Redwa/Capstone/blob/master/img/wordcloud2.png)

## 4- Preprocessing Data

I started the project from a machine learning perspective; Let's Get the data, clean it if necessary, pick up a model and run to get predictions. 

I had a bunch of ideas in mind: clustering, sentiment analysis, classification, graph theory, however I was faced by the real issue how to classify these tweets to make sense of them before starting modeling. 

Data Science is multidisciplinary: Math, Coding, and Specific Business Expertise. Somebody who seek intelligence from the dataset should have an idea on not only how ISIS and alike use twitter but what is their ideology and pitch too.

** I decided to label the tweets into three categories:

   • a- N: News

   • b- O: Opinions and Chats

   • c- I: Teaching or Informative


** The importance of the labels is to classify the data to get the right information.

** I was also faced with irrelevant data like location. The majority of users hide their locations. Location was not relevant.

** Some user names were changed constantly by adding a letter or a symbol to it. Twitter admin shut down tens of thousands user names related to ISIS in the recent couple years. 

** Not all people in the dataset are ISIS; they are following to know what is going on. Curious people, Law Enforcement, Alert Citizens, Right Wing to name a few.


## 5- Modeling:

## First Approach: Classification Using Sklearn

I ramdomely sampled from the dataset.

I used some features engineering. After carefully looking at thousands of tweets, I replaced the tweets column by three columns 'RT', 'URL', 'Userstart'. 

'RT': If the tweets is retweeted, 1 else 0.

'URL': If it contains a url, 1 else 0.

'Userstart': If the tweet started by a user name, 1 else 0.

Classifiers used:

clf_1 = MultinomialNB()

clf_2 = KNeighborsClassifier()

clf_3 = RandomForestClassifier()

clf_4 = GradientBoostingClassifier()


## Second Approach: Using Tweets Column only to predict the labels

I used sklearn.feature_extraction.text CountVectorizer to get feature names.

Same Classifiers used:

clf_1 = MultinomialNB()

clf_2 = KNeighborsClassifier()

clf_3 = RandomForestClassifier()

clf_4 = GradientBoostingClassifier()


## Results:

Texts analysis using feature_extraction was better in predicting the labels.

![alt tag](https://github.com/Redwa/Capstone/blob/master/img/Slide11.PNG)


## 6- Future work:

•Develop an ISIS vocabulary for sentiment analysis.


•Combine the two mentioned approaches to improve the prediction.

