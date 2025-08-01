## Dataset

The project uses the Million Songs Dataset, which can be found at http://labrosa.ee.columbia.edu/millionsong/. The specific data files used are:

- 10000.txt: Contains user ID, song ID, and the number of times a user listened to a song.

- song_data.csv: Contains metadata for each song, including title, artist name, release, and year.

## Files

PopularityBasedReco.html: This file contains the complete code and analysis for the song recommender. It includes steps for data loading, exploration, and building a popularity-based recommendation model.

## Project Steps

1. **Load Data:** The project begins by loading the necessary libraries and the two datasets (10000.txt and song_data.csv) into pandas DataFrames.

1. **Data Exploration:** The datasets are merged and explored to understand their structure and content. This includes checking the number of unique users and songs.

1. **Data Preparation:** A subset of the data is created for the purpose of building the model. A new column, 'song', is created by combining the 'title' and 'artist_name' columns.

1. **Popularity-Based Recommender Model:** A non-personalized recommender model is built based on song popularity.

   - The model calculates a "score" for each song by counting the number of users who listened to it.

   - Songs are then sorted in descending order based on this score to determine the most popular songs.

   - The top 5 songs are identified as the recommendations.

1. **Making Predictions:** The popularity-based model is used to generate recommendations for a list of sample users. The recommendations are the same for all users, as the model is not personalized.
