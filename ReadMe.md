# WeRateDogs Twitter Data Wrangling & Analysis
This project was completed as part of Udacity's Data Analyst Nanodegree.

[WeRateDogs](https://twitter.com/dog_rates?ref_src=twsrc%5Egoogle%7Ctwcamp%5Eserp%7Ctwgr%5Eauthor) is a Twitter account that posts and rates pictures of dogs. 
 Most of the necessary Twitter data has been provided by Udacity and includes information on each post, as well as details on each dog such as the name, rating, and stage (whether the dog is a doggo, floofer, pupper, or puppo). See below for definitions on the dog stages. However, not all of the desired data is present in Udacity's dataset, so I also use the Twitter API to gather additional data.

![Dogtionary](/visualizations/dogtionary.png)

In addition, Udacity ran the images on WeRateDogs's account through a neural network to generate three predictions for each image. For each prediction, there is also data on the confidence and whether the prediction is a type of dog breed.

In the data wrangling process, I assess the data for cleanliness and tidiness issues and clean the data as needed so that it is in an adequate form for my analysis. I also provide a brief analysis using the cleaned data. In the analysis, I aim to answer the following questions:
- Aredog generally rated favourably or not?
- What are the most popular dog names based on number of posts, interactions by Twitter users, and ratings?
- Is there any correlation between likes and retweets by Twitter users?

## Requirements
- Jupyter Notebook
- Pandas
- Numpy
- Requests
- Tweepy
- json
- Matplotlib
- Scipy
- Twitter API

## Installation
To get the Jupyter Notebook running, execute the following in the command line and select `wrangle_act.ipynb` from the Jupyter Notebook dashboard. The conda environment setup is optional; I have provided the base environment in `base.yaml`.
```
$ git clone https://github.com/evanchen13/weratedogs.git
$ cd weratedogs
$ conda env create -f base.yaml
$ jupyter notebook
```

`image-predictions.tsv` is provided in this repository, but can be downloaded programmatically as shown in the code. Similarly, `tweet_json.txt` is provided in this repository, but can be downloaded programmatically using the Twitter API. This requires a developer account. To apply for access, visit this [link](https://developer.twitter.com/en/apply-for-access) and click the "Apply for a developer account" button. Then, be sure to edit the following lines in cell 5:
```
consumer_key = 'CONSUMER_KEY'
consumer_secret = 'CONSUMER_SECRET'
access_token = 'ACCESS_TOKEN'
access_secret = 'ACCESS_SECRET'
```
