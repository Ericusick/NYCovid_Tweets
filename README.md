# NYC Covid-19 Cases and Twitter
Using Twint to filter through Covid related tweets from New York City to see if the message of a verified users affects the Covid infection/cases rate in NYC. In this project NLP and Random Forest Regressor will be utilize to see if there is any words that have a higher correlation with new Covid cases.

# Twint
[Twint API](https://github.com/twintproject/twint/wiki) is used to gather all of the tweets that is related to Covid found in New York City.
Some input parameters to obtain the desire tweets are:
- Location: New York City
- Date: 01/01/2020 - 02/14/2021
- Verified User
- Likes count greater than 50

The following words were used as search word to obtain the tweets:
- Covid
- Corona
- Coronavirus
- Mask
- Vaccine
- Quarantine

All desire tweets were compile into a csv file named 'covidtweets.csv' which contains approximately 3000 tweets

# NLP
NLP needed to be done to the tweets data before it can be used to model. Some of the cleaning that was done are:
- Removing hashtag symbol, url links, @username, punctuations, and digits 
- Tokenization was used to break up the tweets into a list
- Stopwords was used from the NLTK library to get rid of unnecessary or meaningless words
- Lemmatization was used to break down the words to it root form (for example: studying, studied, and studys were break down into study)
- Count Vectorize was use to count each individual words and compile all of the tweets from the same date into a single row.

# New York City Cases
After taking care of the text data, we will Covid cases data from NYC. Luckily The New York Times provide such dataset for anyone to use and is constantly update new reports nationwide. The dataset provide by [NYTimes](https://github.com/nytimes/covid-19-data) was modify to be new cases only found in New York City since that what we were most interested in. 

A graph of new Covid cases found in NYC:
