# spotify-recommendation-engine
generate the most related songs to your favorite song in spotify!

      - Data Exploration
Make data exploration easier by using ('display.max_columns', None) and ('max_rows', None)

- put a regex statement together to extract the genre and store it into a list.
- create song identifier because we have duplicate songs, then sort them and drop the duplicates songs.
 
- use (.groupby) to group the songs id and create lists of them.

- remove the duplicated songs from the dataset with (.drop_duplicates) 
- groupby songs id and create lists to be consilidate next and output all of the unique values

- create OHE features with a function, then build the feature set with a function 

        - connecting to spotify API
- get playlist  names and their images, then generate playlist dataframe

- pull songs from a specific playlist with a function that pull them by (playlist_name, id_dic, df)

1- playlist_name: the name of the playlist we would like to use from spotify API

2- id_dic : the dictionary that maps ( playlist_name ) to ( playlist_id )

3- Df : spotify dataframe

- Visualize cover art of the songs in the inputted dataframe

#generate playlist feature(complete_feature_set, playlist_df, weight_factor)

1- complete_feature_set … pandas dataframe which includes all of the features for the spotify songs

2- playlist_df… playlist pandas dataframe

3- weight_factor… float value that represents the recency bias. The larger the recency bias, the most priority recent songs get. Value should be close to 1


      - Generate Recommendations 
  
Pull songs from a specific playlist with a function

    1- df (pandas dataframe): spotify dataframe
    2- features (pandas series): summarized playlist feature
    3- nonplaylist_features (pandas dataframe): feature set of songs that are not in the selected playlist
Returns:
    non_playlist_df_top_40: Top 40 recommendations for that playlist

- finally, get the recommendations.

