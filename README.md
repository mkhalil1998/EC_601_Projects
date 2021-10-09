# EC-601-Twitter_Project

Phase 1 a: Exploring the twitter API
--------

TwitterProject-Phase1.py allows the user to extract the most recent twitter posts for a particular user. 
The code also cleans the data so that it is ready for the next step of NLP. 

Testing: The code was tested with extracting the most recent twitter posts from Cristiano Ronaldo and they were compared to the tweets on twitter.


Phase 1 b: Exploring the Google NLP API 
--------

TwitterProject-Phase1b.py allows the user to use the extracted text from twitter that can be done using TwitterProject-Phase1.py and input it to the new function entiment_analysis_tweets. According to the generated sentiment score, the tweet is categorized into one of the sentiment levels. 
 
 - 0.3 - 1 -> Positive 
 - 0.3 - -0.3 -> Neutral  
 - -0.3 - -1 -> Negative 
 
Testing: The code was tested with extracting the 10 most recent twitter posts from the White House and each post was given a sentiment level. 

Phase 2: Product Mission
--------

### User:
As a sales manager, I want to understand if customers are enjoying the product so that I can pin point improvements for the next release. I don't want to rely only on amazon/google reviews but also wants to analyze tweets. By looking at tweets about the product, and focus mainly on the ones that are tagged as negative by the sentiment analysis API. 

As a customer, I am interested in buying a product and want to get an idea on what people think about it, as well as take a closer look at tweets that have both have very positive or very negative sentiment. 

### MVP: 
The product should be able to provide the user with the following:  
 - Tweets about specified product
 - Sentiment Analysis for generated tweets 

In addition to this main two requirements, I believe that information such as date and location can provide also important insights to the user, these can be added to the both the query as well as outputs. 

### Modules: 

1- twitter_api_module.py: 
This modules has two primrary functions. It extracts the tweets related to the specified product and number of tweets. It also cleans/preprocesses the data to prepare it for sentiment analysis.

Steps done to clean the tweets are as follows: 
 - Converting all letters to either upper case or lower case.
 - Stopword removal: Some words do not contribute much to the machine learning model, so it's good to remove them. A list of stopwords can be defined by the nltk library, or it can be business-specific.
 - Remove user @ references and '#' from tweet
 - Remove punctuations
 
An example of the output of this module is as follows: 
![alt text](https://github.com/mkhalil1998/EC-601-Twitter_Project/blob/main/Images/module1.png)
