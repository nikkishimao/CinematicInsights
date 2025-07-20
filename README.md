<h1>Mini Project: Cinematic Insights</h1>

<h2>Introduction</h2>

<p>In this mini project, Cinematic Insights, a merged dataset of movie details and user ratings is analyzed to uncover certain trends and insights into the data that can be used to make one’s own decisions about watching specific movies. Initially the two data sets, movies and ratings, which are sourced from Kaggle, are imported, cleaned, and reformatted. The movies data set is reformatted so that it was more visually pleasing, the release year was extracted to become its own column, and some unnecessary characters were removed. The ratings data set was cleaned by ensuring that there were no duplicate ratings, and its timestamps were converted to datetimes and saved as a new column. These two datasets were merged on a common movieId to tackle three key analyses. The first is to identify the highest rated movies in the Drama/Romance genre. The second is to compare the first and last ratings of the movies in order to highlight those with significant rating increases. Lastly, this project examines User 19’s ratings by calculating their average rating, lists their 5-star movies, and identifies their lowest rated films. Overall, this project provides valuable tools for movie enthusiasts to make informed viewing choices whether it’s based on the genre they prefer, how certain movies’ ratings improved over time, or the personal recommendations of a specific user.</p>

<h2>Part 1: Data Cleansing</h2>

<p>In Part 1 of this project, the two datasets (movies and ratings) were imported and cleaned for analysis. The movie data was initially checked for data types, missing values, and duplicates. The genres column, which originally used the (|) character, was reformatted to use commas instead. Additionally, the year was extracted from the movie title and stored in a new column, while the year was removed from the title itself. The display settings were adjusted to ensure that the movie data could be viewed clearly.

<p align="center">
  <img src="https://github.com/nikkishimao/CinematicInsights/blob/fd7fa92a94bc02bc38bc0a9c848c46afa1a44f3c/images/Part1_1.png" width="500" />
</p>

<p align="center">
  <img src="https://github.com/nikkishimao/CinematicInsights/blob/fd7fa92a94bc02bc38bc0a9c848c46afa1a44f3c/images/Part1_2.png" width="700" />
</p>

<p align="center">
  <img src="https://github.com/nikkishimao/CinematicInsights/blob/fd7fa92a94bc02bc38bc0a9c848c46afa1a44f3c/images/Part1_3.png" width="700" />
</p>

For the ratings data, missing values and duplicates were checked, and a column was created to convert the Unix timestamp into a readable datetime format. After cleaning, both datasets were saved as separate data frames (cleanmovies_df and cleanratings_df) for further analysis. These steps ensured that both datasets were properly formatted and ready for merging, along with deeper analysis.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/CinematicInsights/blob/a53019c197de02a264c5446a044200b3424e437e/images/Part1_4.png" width="500" />
</p>

<p align="center">
  <img src="https://github.com/nikkishimao/CinematicInsights/blob/a53019c197de02a264c5446a044200b3424e437e/images/Part1_5.png" width="700" />
</p>

<h2>Part 2: Merging Datasets</h2>

<p>In Part 2, the cleaned movies and ratings datasets were merged into a single dataset. The two datasets were joined using the common column, movieId, which is present in both cleanratings_df and cleanmovies_df. An inner join was performed to ensure that only rows with matching movieId values from both datasets were included in the merged dataset. After the merge, the first and last few rows of the resulting merged_df were displayed to verify the join and ensure that the data from both sources was correctly combined. This step set the stage for further analysis by consolidating the relevant movie details with the associated ratings.</p>

<p align="center">
  <img src="https://github.com/nikkishimao/CinematicInsights/blob/0c383ff2031f4427a046fea957ee27e95efdb2aa/images/Part2.png" width="700" />
</p>

<h2>Part 3: Questions</h2>

<h3>Question 1</h3>
<p>In Part 3,  the three comparison questions were answered and even further investigated with follow-up questions. For the first question, the analysis aimed to identify the movies with the highest average ratings that belong exclusively to both the Drama and Romance genres. The final output was a list of movies that met the criteria: the highest average ratings and belonging exclusively to both the Drama and Romance genres. These movies were displayed in order from the earliest to the most recent year, along with their titles, average ratings, and genres. The steps involved:</p>

<p align="center">
  <img src="https://github.com/nikkishimao/CinematicInsights/blob/59c0d21231f71fc731b920eb15318389a515b027/images/Part3_1.png" width="700" />
</p>

<p align="center">
  <img src="https://github.com/nikkishimao/CinematicInsights/blob/59c0d21231f71fc731b920eb15318389a515b027/images/Part3_2.png" width="700" />
</p>

<p align="center">
  <img src="https://github.com/nikkishimao/CinematicInsights/blob/59c0d21231f71fc731b920eb15318389a515b027/images/Part3_3.png" width="700" />
</p>

<h3>Question 2</h3>
<p>Then for Question 2, the analysis focused on comparing the first and last ratings of each movie and identifying movies where the rating increased by at least 4 between the first and last rating. The output revealed a list of movies where there was a noticeable increase in ratings (at least 4), along with the details of each movie's first and last rating and the datetime of when those ratings were made. The steps involved:</p>

<p align="center">
  <img src="https://github.com/nikkishimao/CinematicInsights/blob/bb6809abfc04c12f0bf4f1842ab225ec303d1ba8/images/Q2_1.png" width="700" />
</p>

<p align="center">
  <img src="https://github.com/nikkishimao/CinematicInsights/blob/bb6809abfc04c12f0bf4f1842ab225ec303d1ba8/images/Q2_2.png" width="700" />
</p>

<h3>Question 3</h3>
<p>Lastly, for Question 3, the analysis focused on examining the movie ratings given by User 19 (userId = 19). The analysis revealed User 19’s overall average rating, highlighted the movies rated 5 stars, and listed the 50 movies they rated the lowest. This provided insights into the user's preferences and tendencies in movie ratings. Also, User 19 was investigated due to my choice, but in theory similar code and examination can be done to any user amongst the dataset, which just further shows how to helpful and customizable this project can be. The steps involved:</p>

<p align="center">
  <img src="https://github.com/nikkishimao/CinematicInsights/blob/000b62a8440ab4f9afa0738cca3c5a4f433559de/images/Q3_1.png" width="700" />
</p>

<p align="center">
  <img src="https://github.com/nikkishimao/CinematicInsights/blob/000b62a8440ab4f9afa0738cca3c5a4f433559de/images/Q3_2.png" width="700" />
</p>

<p align="center">
  <img src="https://github.com/nikkishimao/CinematicInsights/blob/000b62a8440ab4f9afa0738cca3c5a4f433559de/images/Q3_3.png" width="700" />
</p>

<h2>Conclusion</h2>
<p>This mini-project, "Cinematic Insights," analyzed movie ratings to uncover patterns in viewer preferences. By merging datasets and addressing key questions, we identified top-rated Drama/Romance films, explored how ratings evolve over time, and examined the viewing habits of User 19. Ultimately, this project highlights the value of data analysis in understanding movie trends and helps viewers make informed choices about what to watch based on ratings.</p>

<h3>Full Code and Conclusions in more Detail</h3>
<ul>
  <li><a href="code/miniproject_shimao.ipynb">Full Code Breakdown</a></li>
</ul>


