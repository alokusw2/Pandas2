# Pandas2
1 Problem 1 : Article Views I	(	https://leetcode.com/problems/article-views-i/  )

Write a solution to find all the authors that viewed at least one of their own articles.

Return the result table sorted by id in ascending order.

The result format is in the following example.
------------------------------------------------
import pandas as pd

def article_views(views: pd.DataFrame) -> pd.DataFrame:
    df = views[views['author_id'] == views['viewer_id']]
    return df[['author_id']].drop_duplicates().rename(columns={'author_id': 'id'})



2 Problem 2 :Invalid Tweets	(	https://leetcode.com/problems/invalid-tweets/ )

Write a solution to find the IDs of the invalid tweets. The tweet is invalid if the number of characters used in the content of the tweet is strictly greater than 15.

Return the result table in any order.

The result format is in the following example.

------------------------------------------------
import pandas as pd

def invalid_tweets(tweets: pd.DataFrame) -> pd.DataFrame:
    return tweets[tweets['content'].str.len() > 15][['tweet_id']]








