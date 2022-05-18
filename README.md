# Are you looking for best hotel to stay? 

[<img target="_blank" src="https://github.com/Data-Fenix/Are-you-looking-for-best-hotel-to-stay/blob/main/hotel_review_analysis.png">](https://github.com/Data-Fenix/Are-you-looking-for-best-hotel-to-stay/blob/main/hotel_review_analysis.png)

## Table of Content
  * [What is sentiment analysis](#what-is-sentiment-analysis)
  * [Dataset](#dataset)
  * [Problem-Statement](#problem-statement)
  * [Motivation](#motivation)
  * [Technical Aspect](#technical-aspect)
  * [Installation](#installation)
  * [Run](#run)
  * [Deployement on Heroku](#deployement-on-heroku)
  * [Directory Tree](#directory-tree)
  * [To Do](#to-do)
  * [Bug / Feature Request](#bug---feature-request)
  * [Technologies Used](#technologies-used)
  * [Contributing](#Contributing)
  * [License](#license)
  * [Credits](#credits)


## What is sentiment analysis?

Sentiment analysis is the technique of capturing the emotional coloring behind the text. It applies natural language processing (NLP) and machine learning to detect, extract, and study customers’ perceptions about a product or service. That’s why this type of examination is often called opinion mining or emotional AI.

The goal of opinion mining is to identify the text polarity, which means to classify it as positive, negative, or neutral. For example, we can say that a comment like

* “We stayed at this hotel for five days” is neutral,

* “I liked staying here” is positive, and

* “I disliked the hotel” is negative.
 
## Dataset

We will use here some hotel reviews data. Each observation consists in one customer review for one hotel. Each customer review is composed of a textual feedback of the customer's experience at the hotel and an overall rating. The data can be found here: https://www.kaggle.com/jiashenliu/515k-hotel-reviews-data-in-europe


## Problem Statement
For each textual review, we want to predict if it corresponds to a good review (the customer is happy) or to a bad one (the customer is not satisfied). The reviews overall ratings can range from 2.5/10 to 10/10. In order to simplify the problem we will split those into two categories:

* bad reviews have overall ratings < 5
* good reviews have overall ratings >= 5
The challenge here is to be able to predict this information using only the raw textual data from the review. Let's get it started!

## Motivation

When I was searching about AWS Sagemaker, I struggle a lot as lack of references in this feild. It has some references, but there are missing few things. Therefore I need to fullfil that gap. So now I have some experience in this feild and as a MLOps team memeber, I migrated a lot of projects into cloud. I saved data scientists' valuable time by automating and scheduling their ML projects. So now I need to share that experience and knowledge with you and this is my first step of that journey.

## Technical Aspects

<b> Step 1 </b> — data collection. First, you have to gather real reviews left by hotel guests. The best way to do it is to use feedback from your website. If this option is unavailable, you may try to partner with resources that have ownership of such data. The common method of collecting datasets — scraping — is not recommended as it may entail legal issues. Under the GDPR and CCPA rules you can’t apply this technique to personal data. You also may unwittingly violate property rights of website owners.

<b> Step 2 </b>— sentiment annotation. To make opinions hidden in a review visible to machines, you need to manually assign sentiment labels (positive, neutral or negative) to words and phrases. Data labeling for sentiments is considered reliable when more than one human judge has annotated the dataset. The rule of thumb is to engage three annotators.

<b> Step 3 </b>— text cleansing. Raw hotel reviews contain tons of irrelevant or just meaningless data that can badly affect model accuracy. So, we need to clean them up, which includes:
* removing noise — or things like special characters, hyperlinks, tags, numbers, whitespaces, and punctuation;
* removing stop words which include articles, pronouns, conjunctions, prepositions. etc. One of the most popular NLP libraries, NLTK (acronym for Natural Language Toolkit) lists 179 stop words for the English language;
* lowercasing to avoid lower case/upper case differences between words with the same meaning;
* normalization — or transforming words into a canonical form. For example, a normalized form of 2morrow and 2mrw is tomorrow;
* stemming or reducing each word to its stem by chopping off endings (prefixes and suffixes). The technique often produces grammatically incorrect results — for example, having will be stemmed to hav; and
* lemmatization — meaning returning a word to its dictionary form. Say, the lemma for swimming, swum, and swam is swim.


## Installation

#### Requirements

1. Python 3.5+

#### Required Libraries

* pandas
* sklearn
* nltk
* string
* gensim
* seaborn
* matplotlib
    
## Run
1) Upload/push/clone previously implemented mobile price prediction project into your JupyterLab environment.
2) Execute Hotel Review Sentimental Analysis.ipynb


## Directory Tree

```
├── Hotel Review Sentimental Analysis.ipynb
├── README.md
└── hotel_review_analysis.png
```

## To Do

Need to add,
1) Need to deploy this project in AWS platform

Don't worry, we will discss above topics and many more in the future sections.

## Bug / Feature Requests
If you find a bug (the website couldn't handle the query and / or gave undesired results), kindly open an issue [here](https://github.com/Data-Fenix/how-do-we-earn-more-than-50K-per-year/issues/new) by including your search query and the expected result.

If you'd like to request a new function, feel free to do so by opening an issue [here](https://github.com/Data-Fenix/how-do-we-earn-more-than-50K-per-year/issues/new). Please include sample queries and their corresponding results.

## Technologies Used
[<img target="_blank" src="https://logos-world.net/wp-content/uploads/2021/10/Python-Symbol.png" width=200>](https://logos-world.net/wp-content/uploads/2021/10/Python-Symbol.png)

## Contributing

<p><b> ML Enginner </b> : Anuradha Dissanayake </p>
<p><b> Data Scientist </b>: Shashi Withanage </p>

## License

Copyright 2022 Anuradha Dissanayake and Shashi Withange

## Credits

1) https://www.kaggle.com/code/jonathanoheix/sentiment-analysis-with-hotel-reviews/notebook
2) https://www.kaggle.com/code/suyogdahal/hotel-reviews-sentiment-analysis/notebook
3) https://www.altexsoft.com/blog/sentiment-analysis-hotel-reviews/
