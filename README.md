# Data_Wrangling-WeRateDogs
Performing Data gathering, assessing and cleaning on data collected using twitter API from "WeRateDogs" page

## Wrangle Report

The data wrangling project was challenging for me and I learned a lot about the data gathering process, data assessing, data cleaning process and also the Twitter API.
I gathered data from three different sources for this data analysis. WeRateDogs gave Udacity exclusive access to their Twitter archive for this project in the form of a csv file. The archive contained basic tweet data for their tweets as they stood on August 1, 2017.
Each tweet image was run through a convolutional neural network to analyze the images of dogs and correctly identify their breeds.
The convolutional neural network predictions was downloaded programmatically by me using the Requests Python library as a tsv file. And finally by using the tweet IDs from the WeRateDogs archive I queried the Twitter API for each tweet's JSON data using the Python’s Tweepy library. I stored each tweet’s entire set of JSON data, which
I would later use to analyze the tweet’s retweet and favorite counts.
The most difficult part of the project was data gathering process, specially querying the Twitter API which was a challenge for me.
The Twitter API syntax was the most challenging and in my efforts to work through the problem.
I discovered that the support documentation for the Twitter API is confusing, especially for people who are trying to learn how an API works for the first time.
Once I had successfully gathered all the data, I copied the files for the assessment and data cleaning processes. I evaluated the dataframes, looking for quality and tidiness issues and then I began to fix them. I began the Cleaning process by addressing missing data and mislabeled information, which was mostly found in the WeRateDogs Twitter archive. I then converted columns to a proper data format, primarily changing the timestamp data into datetime objects, tweet_id from a number into a string and the rating columns into float
objects. Then I corrected the name of some dogs which were None to Nan. The next step for me was to fix the records which had a zero in the denominator as it was a serious issue.
I also figured out that there were some missing urls in the twitter archive file, I decided to delele these records as they were not many in number and there was no way to figure out the link.
Then I came across the issue of retweets that I had to remove because they were of no use for our analysis. While assessing the dataset I realized that there was some wrong data in the ratings column and there was no way to figure out the right value so I had to delete those records.
It looked like the regular expressions used had got these rating and the correct data was not provided in the tweets.
There were some invalid names like a, an, the, very, one, just, quite, getting, mad, actually, incredibly, such, light, this, by, infuriating, officially, old, my, all, his, space, life, unacceptable
and so on so I decided to remove these records.
Some rating in the denominator had rating more than 10 so I had no normalize those values to make some sense out of them.
Also I found out that there were a few records which had the rating in decimals so I changed the datatype to support that type of format and I also corrected those ratings.
The final step in the data cleaning process was data tidiness issues such as combining the dog breed column from four columns to one. I also decided to join all the tables together
using an inner join all three datasets into a final document containing all relevant information.
In summary, this project was the most challenging one in this nanodegree, specially using the Twitter API to gather the JSON data. Overall, this project was completed successfully and I’m extremely grateful with the new skills I have acquired. A special thanks to Udacity for making this project a part of our nano-degree programme, and a special thanks to my mentors who were there with me in the entire journey.
