![Concert_hall_rock_concert-1366x668 (1) (1)](https://user-images.githubusercontent.com/93050931/160220252-cf9e1863-fb74-4833-b9ad-bdfc3e844efb.jpg)






# Group 11: Spotify Song Popularity Predictor

## Creating a More Diverse Musical Landscape with Machine Learning
Music can bring people together. That's what the members of our team agreed upon and because all of us share a passion for music along with the creativity of the artists that create it, we decided to create a machine learning algorithm that could improve today's musical landscape. With the rise of big data, our group wondered how increased insights into listener preferences may influence the music that acheives the most success. If data analytics shows that a certain song style or genre has a higher chance for popularity, isn't it likely that the mainstream will be saturated with that genre? This scenario would result in artists foregoing creativity in favour of profits and a popular music landscape that lacks variety.
This in turn motivated us to try to find an optimal dataset for this project and found a Spotify dataset containing over 200,000 songs including metrics for songs popularity as well as musical element such as loudness, danceability, energy, key, etc. We believe that Spotify is an optimal source of data as it is one of the largest and most popular music-streaming services and so, will likely represent popular musical tastes fairly well.

## Purpose of the Project:

As mentioned above, our team wants to address the impact that big data could have on the diversity of mainstream music. If we were able to show what makes a song successful in less popular genres with our algorithm, smaller artists in those genres could be assisted in reaching wider audiences. Thereby increasing mainstream interest in the genre whilst helping small artists find more financial success.

For our project we chose to create a Random Forest regression machine learning model that could predict the popularity of any given song provided with the following criteria. In this dataset, popularity is scored on a scale of 1-100 based on listen counts of each song relative to the listen counts of other songs on Spotify:

- acousticness 
- danceability 
- duration 
- energy
- instrumentalness 
- key 
- liveness 
- loudness
- mode
- speechiness
- tempo
- time signature
- valence



We intend to subset our database of songs to a single genre to figure out how the criteria listed above contributes to the popularity of a song in that genre specifically.


## Source Data
Our source data is a dataset from Kaggle called 'SpotifyFeatures.csv'. The dataset contains the name, track_id, genre, and artist name of 232,725 songs along with the target and feature variables listed in the 'Selected Topic' section of this README file. The songs listed in this dataset were all released in 2019 or earlier. The data contains no missing values but has many duplicate values which will need to be dropped from our dataset before using it. 

## Used Technologies :
-Postgres.
-Python ,jupyter Notebook.

## About the Database 
### March 20, 2022 notes
* Created ERD and schemas for dataset, splitting SpotifyFeatures.csv into two tables one for associated information per track ID and another for the track's audio features.
* [Images](/images/) of the provisional Postgres database with sample data provided.
* The resulting table joined on track_id can be exported as CSV to be used downstream for the machine learning model:
```
SELECT * 
FROM track_metadata as tm
INNER JOIN track_features as tf
ON (tm.track_id = tf.track_id)
```

## Questions to be  answered:
1. Our main question, what mix of sonic qualities make a song more popular in any given genre?
2. Which metrics have the highest impact on song popularity? Which has the least effect?
3. How does mean song popularity vary from genre to genre? Can we create a tiered-list of the most popular genres?
4. How much variance is there between the "ideal" song in each genre? Which genres are the most or least sonically similar?
5. Is it possible to assign a genre to a song accurately using the metrics used as feature variables for our algorithm

## Communication Protocols
Prior to designing our project each member shared their availability for all 7 days of the week with the rest of the group in a Whatsapp group chat. During this project, written communication will take place on the aforementioned Whatsapp chat as well as the Group chat on Slack which includes our Teaching Assistant for the project, Jose. For vocal communication, our group will be meeting every Tuesday and Thursday for our scheduled class as well as scheduling additional meetings on the weekend as necessary. Information and documents that each member would like to share can also be posted to a group Google Docs document which has allowed for collaboration on designing the project and machine learning model. Additionally, each group member has been added to a GitHub where we can upload our work and comment on other's code.
