# About:
The aim of this thesis is to understand the Twitter users whether the user is bot, troll, commercial user,
regualr user by summarizing the timeline information of a Twitter user.


# About the data:
We have crawled the data using Twitter API. The dataset consist of a total of 124 users, among them 35 users
are bots, 28 are commercial users, 32 users are regular users and 29 are troll accounts.
The dataset can is available in "dataset/crawled data" folder.


# Implementation:
- Intially crawling the dataset, we have crawled the data for 124 user, for each user 3 months data has been collected.
The source code for crawling the data can be found in "source code/Twitter data crawling". 

- After crawling the dataset, we have analyzed individual profile by perfomrming EDA and merged the dataset which we
assume to be bots, trolls etc, and created ground truth based on the observed patterns and rules used. We have also performed 
feature engineering for converting raw data into more meaningful format, for example finding similarity between 
retweets and favorites, finding time differnce between each tweet for understanding trend or regularity in the data etc,
Finally we have converted 3 months data of each user into one row format per user, with only the features which provide more
information, and used this data for clustering, classifiaction, etc.
The code can be found in "source code/Analyzing individual profile and feature engineering". 

- Using the merged data, we performed EDA on merged data for better visualization and summarization of information,
besides this, we have performed data clustering, classification and evaluated the model. The merged datasets for bot,
troll etc, will be available in "dataset/merged datasets".
The code for this will be available in "source code/EDA-clustering-classification-evaluation".
The results of clustering, correlation matrix, classifiaction report, confusion matrix are all will be available
in this code.
along with this we have analyzed frequency of tweets per day and per month for both bots, and regular users. The
data set is available in "dataset/crawled data/bots" and code is available in "source code/EDA/bots-tweet_frewuency" 

- One of the features used to understand Twitter users is sentiment of tweets, for annotating the sentiemt for the
the tweets, we have used Vader sentiment tool. To cross check how well this tool is annotating sentiment we have used
pre trained bert model for fine tuning the results obtained from sentiment tool. The dataset of tweets along with
sentiment assgigned by vader tool can be found in "dataset/crawled data/merged datasets/tweets for BERT sentiment 
analysis". The code for bert fine tuning can be available in "source code/ BERT for fine tuning sentiment".

- To be very precise in creating ground truth, some rules which we have used to understand Twitter user, are 
evaluated by analyzing the existing bots dataset. We have analyzed two existing bot datasets, the dataset are 
avialable in "dataset/existing data" and code is avilabele in "source code/Analysis of existing datasets"  


### Setup:
- The Twiiter crawling, individual profile analysis, EDA, clustering, classification, can be run using jupyter notebook,
Bert sentiment analysis had run using google colab, since we had to use GPU for training. 

- For analysing the frequency of tweets for bots, and trolls we need to load all datasets of 35 users and 3 months 
dataset of each user need to be used.  

- Existing datasets analysis were also run using google colab, therefore the dataset path needs to be changed while
running the code on existing data. 
 
