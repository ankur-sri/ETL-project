# ETL-project
Extract Transform and Load Project

Purpose: Find data from different data sources, clean the data, and combine them into a database.

Thesis: Our group wanted to determine the most popular video game console of all time in terms of sales of the individual consoles and total sales of video games for each console.

Extract: We selected two data sources one from Kaggle (https://www.kaggle.com/ashaheedq/video-games-sales-2019) which is a list of all video game sales from 1980 to 2016 and the other was a scrape of data from Wikipedia (https://en.wikipedia.org/wiki/List_of_best-selling_game_consoles) of the best selling video game consoles of all times. For the rest of the paper we will refer to the video game sales dataset as “games” and the best selling console dataset as “consoles”.  We turned these into .csv files and loaded them into Pandas Dataframes.

Transform: Cleaning the data was a far more monumental task than we would have guessed.  It required a complicated sorting algorithm (See comment in code #Cleaning Algorithm) to update the platform name from the consoles Dataframe to match the platform name of the games dataset.  Some of the information in the console dataset were deemed as estimates of a range.  Instead of writing a code to extract and modify this data, we chose to make a clean .csv file (Wiki_Scrape_clean.csv) and marked the rows we modified for clarity and posterity.  As we began working on the data we decided to simplify our dataset and only display video game consoles which sold over 10 million units.

Load: With the two Dataframes having same key values, it was elementary to combine them.  By using the groupby() and sum() functions we have a very clean and simple Dataframe which displays total video game sales of consoles that have sold at least 10 million units.

Conclusion: Finding good datasets is of the utmost importance when working with combining disparate information.  We spent the majority of our time cleaning the key values so they matched on the Dataframe join.  With how much time it took just to combine a two sources of data into a single dataset we can only imagine how difficult it would be for even more diverse 
