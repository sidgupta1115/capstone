# Can machine learning techniques solve the epidemic of fake news?
## Approaches to News classification and recommendations for building a production grade News Classifier

### Motivation

Since the 2016 election "fake news" has spread through our public discourse and public trust in the media has dramatically declined. I've been an avid follower of the news since the 2016 campaign and I've been pretty sensitive to how the publications I subscribe to inform my opinion. I wanted to see how sensitive machine learning algorithms could be to detectivng biases in news.



## Problem Question
If there is a standard set of classes for news that reflect an article's trustwortiness, 

1. How can you make a news classification model with a labeled set of data? 
2. What features would be most important for this model?
3. What would be the architecture and needs for a production sized news classifier?

## Datasets

I will be working with two datasets one from kaggle and from George McIntire opendatascience blog post as they contain different fields lend themselves better to separate analysis.

1) Kaggle- 12,999 entries: "contains text and metadata from 244 websites and represents 12,999 posts in total from the past 30 days. The data was pulled using the webhose.io API [...] Each website was labeled according to the BS Detector as documented here: https://github.com/selfagency/bs-detector. Data sources that were missing a label were simply assigned a label of "bs". There are (ostensibly) no genuine, reliable, or trustworthy news sources represented in this dataset (so far), so don't trust anything you read."

#### Kaggle Data Dictionary- Features to note
- **published**: date/time published (10-26-16 to 11-25-16)
- **title**: title of article
- **text**: : text of article
- **language**: data from webhose.io 
- **site_url**: site URL from BS detector 
- **replies_count**: number of replies 
- **participants_count**: number of participants 
- **likes**: number of Facebook likes
- **comments**: number of Facebook comments
- **shares**: number of Facebook shares
- **type**: type of website (label from BS detector) "bs", "bias", "conspiracy", "hate", "satire", "state", "junksci", and "fake" **No "real" labeled articles**


2) McIntire dateset- 6335 entries labeled either "REAL" or "FAKE". "REAL" articles scraped from Allsides.com, a website dedicated to hosting news and opinion articles from across the political spectrum. Articles on the website are categorized by topic and by political leaning (left, center, and right). "REAL" articles were from 2015 to 2016 and came from media the organizations the New York Times, WSJ, Bloomberg, NPR, and the Guardian. "FAKE" articles are a random subset of "bs" articles from the kaggle dataset. The data has a 50% split in the class labels

#### McIntire Dictionary
- **title**: title of article
- **text**: : text of article
- **label**: "REAL" or "FAKE"

See a slide deck with my findings:
https://docs.google.com/presentation/d/1b4ykKEwQ9kdYyBhNIDnEdiScvyagiGzVclTBqU48e9k/edit#slide=id.gc6f980f91_0_0
