# Anime Recommendation System - Collaborative Filtering Project
![](images/dataset-cover.png)


For this project I chose to do another anime related project. Specifically to make a recommendation system to find the similarity between shows and users to suggest comparable anime shows, users and to predicted a user's ratings.


The Data:

I used a csv file I cleaned from a previous project, where I had dropped all the hentai anime. I'm not interested in that for this project. Maybe later... ended with 5,561 unique anime data points and a few entries that were not usable. I also used another csv file from kaggle which contained  User Ratings for animes, User ID's and anime ID's, this was used for the in conjunction, collaborative, with the anime dataset.

## What Did I Do?

* Load and Prepared Data

  - Imported .cvs files, into pandas dataframes

  - Separated dataset to only include Anime TV shows, Didn't want to include movies.

  - Merged both dataframes on the shared animeID column. As well as drop all non-rated user ratings.

* Did some Exploratory Data Analysis:

  ![](images/EDA.png)

  - Plotted the relationship between User Ratings and total amount of User for each rating (1-10), across all animes.
  ![](images/Usercount-Rating.png)


  - Visualized the Count of Ratings Per Anime (Filtered up to 300 Ratings per Anime
  ![](images/Ratingcount-Anime.png)

  - Visualized the Count of Ratings Per User (Filtered up to 300 Ratings per User
  ![](images/Ratingcount-User.png)

* Filtered the dataframe

  - Limited dataframe size to include value counts greater then a min value count(50) of anime_id and user_rating, mainly for computing reasons.

* Created Matrix - The start of the recommendation system

  - Pivoted the table to show User_ID's on one axis and the Anime TV Shows across the other. This allowed me to chart the User Ratings by User_ID's and Anime.

  - Transposed and converted the matrix to a sparse matrices

* Computed the the similarities

  - I ran the spared matrix and transposed matrix through cosine_similarity to find the anime and user similarities

  - Inserted the 2 similarity matrices into separate dataframes

* I made functions to call for the recommendations of:
  - Top Similar Animes
  - Top Similar Users with similarity values
  - Similar User Ratings
  - Predicted Rating of a Anime and a User specified.

* Lastly I made a Function to calculated the Mean Square Error and the Root Mean Square Error of the Predicted Rating of a Anime and a User specified, mentioned above.


Hope You'll enjoy my Anime Recommendation - Collaborative Filtering Project

## Built With

* Python3.8
* Jupyter Notebook 6.0.0
* A few of the main imports: pandas, numpy, pyplot, scipy, sklearn


## Authors

* **Samuel Diaz** - *Creator* - [sdman135](https://github.com/sdman135/) - [LinkedIn](https://www.linkedin.com/in/samuel-diaz-data-scientist)
