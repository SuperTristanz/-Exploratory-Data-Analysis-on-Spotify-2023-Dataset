# Exploratory-Data-Analysis-on-Spotify-2023-Dataset
## Data set was Retrieved from Kaggle ((https://www.kaggle.com/datasets/nelgiriyewithana/top-spotify-songs-2023)
### Author: Angostora, Tristan Zeth V. 
### Program Adiser/s: 
### Section: 2ECE-D


## Exploratory Data Analysis
#### In this deliverable, you will perform an exploratory data analysis (EDA) on a dataset containing information about popular tracks on Most Streamed Spotify Songs 2023 . This task aims to analyze, visualize, and interpret the data to extract meaningful insights.

## GENERAL GUIDELINES:
#### Begin by familiarizing yourself with the structure of the dataset. Check for missing values and data types, and perform an initial exploration to understand the different features available.
#### Provide summary statistics to give an overview of key metrics such as the number of streams, release dates, and musical attributes (e.g., BPM, danceability).
#### Use appropriate visualizations (e.g., bar charts, histograms, scatter plots) to uncover trends and patterns in the data. Ensure that your plots are well-labeled and easy to interpret.
#### Investigate correlations between different variables and provide insights based on your findings. Explore relationships between streams and other musical characteristics like tempo, energy, or playlists.
#### Based on your analysis, offer any insights or recommendations regarding the tracks, artists, or musical trends that could be useful for understanding what makes a track popular.



##  Libraries that are used to the said Project
#### Pandas & Matplotlib
# ![image](https://github.com/user-attachments/assets/69476d05-cddb-49c8-b5db-ab62fb3899eb)

## Importing the Dataset and Getting its Columns
#### encoding='ISO-8859-1 is used for the jupyter Notebook to correctly interpreted the Dataset
# ![image](https://github.com/user-attachments/assets/cdc38cc2-8398-4b2a-9c81-1677632684b1)

#### Getting its columns for Better visualization What are the columns in the code and what are the Variables of each column
# ![image](https://github.com/user-attachments/assets/fba485ee-adf3-400c-905e-2e669cce9940)

## Overview Of Dataset
### Getting the Number of Rows and Columns
#### Input:
# ![image](https://github.com/user-attachments/assets/9e322a68-61c9-47cd-b443-03476c1e609d)
#### Output: 
# ![image](https://github.com/user-attachments/assets/92c9a3e8-352e-4c91-8fb3-34e4091aae68)
### Getting all the Dtypes and Missing Values
#### Input: 
# ![image](https://github.com/user-attachments/assets/0e0d5efa-023c-4a28-94ab-a66921c7f225)
#### This code creates a summary DataFrame (summary_1) with information of columns present in another DataFrame df. After it extracts the data type of each column and finds the missing values on its own, it merges those two to give full details, which includes Column name Dtype of Missing Value.
#### Output: 
# ![image](https://github.com/user-attachments/assets/915b8686-d6fb-4fa1-abf6-634446cade13)

## Basic Descriptive Statistics
### Getting the Mean, Median, and Standard Deviation of the Streams Column
#### Input:
# ![image](https://github.com/user-attachments/assets/d280f5e6-62b6-4f4b-8561-4e94c640080a)
#### Summary statistics are computed in the code for DataFrame df under the column 'streams.' It calculates the mean, median, and std of all values for this column and saves them in variables with names = "mean," "median," and" std." It then produces a new data frame named summary_2 that compiles those statistics into 2 columns: "Variable" (each entry being either Mean, Median, or Standard Deviation) and the Value of this calculated variable. A new DataFrame summary_2 is created to summarize the central tendency and variability in the 'streams' data.
#### Output:
#### ![image](https://github.com/user-attachments/assets/67b3f832-58b0-4a6f-8a7a-f9ec7192a76d)

### Bargraph for the Mean, Median, and Standard Deviation
#### Input:
# ![image](https://github.com/user-attachments/assets/d593c561-749d-4426-9162-0a7d4f490ffe)
#### By the Graph, it is stated that the Standard Deviation is the highest among the statistical values
#### Output:
# ![image](https://github.com/user-attachments/assets/a5a8ea4b-4415-455b-ba90-22dd620701f8)

### What is the distribution of released_year and artist_count
#### Input:
# ![image](https://github.com/user-attachments/assets/c9647e90-49f9-44a4-a777-664800f31716)
#### For the First subplot, we make it to a histogram to deploy the relationship between the Frequencies or the number of songs produced in the said years 
#### For the Second subplot, we made a boxplot to deploy the relationship between the number of mostly writers, and we can see who or what the number to be considered for it to be an Outlier
#### Output:
# ![image](https://github.com/user-attachments/assets/df08f97c-e9a2-4c7f-93cf-bc71fe6f0701)

### Determining the Outliers
#### Input: 
# ![image](https://github.com/user-attachments/assets/a11a14bb-2b70-49c6-9a34-57b40cb42986)
#### Code to identify outliers in artist count column df using the Interquartile Range (IQR) method. It calculates the first and third quartile of artist_count(Q1, Q3), after which it computes IQR as: (Q3 − Q1). Any value that is 1.5 times the IQR below Q1 or above Q3 defines a lower and upper fence for outliers, respectively. At last, the code filters the DataFrame to identify rows where artist_count lies outside these bounds, resulting in a new data frame summary_3 containing track names, followed by their respective artists and their count of those outliers as per artist_count
#### Output:
# ![image](https://github.com/user-attachments/assets/c0ec2511-a82e-4693-bdc5-bbf2bdd04954)
#### Based on the Table, the highest number for Outliers have 8 artists

## Top Performers
### Top 5 Most Streamed
#### Input:
# ![image](https://github.com/user-attachments/assets/ea12cc44-a4c4-49e2-b9b1-81e508ae5637)
#### The code Determines what is the highest track that is streamed; it selects the track_name, artist(s)_name, and streams columns from the data frame, sorts it in descending order by the amount of streams, and then takes only the first 5 records, using head(). Lastly, it resets the index of our resulting DataFrame to give a clean, sequential index and outputs the DataFrame as a top that contains names of Top Tracks, which are their respective artists & streaming numbers.
#### Output:
# ![image](https://github.com/user-attachments/assets/7f035a60-212f-4110-aaf4-044be32573ec)
### Graph for The 5 most Streamed
#### Input:
# ![image](https://github.com/user-attachments/assets/5e4283d6-ccee-420c-882e-ff27114c012d)
#### Bar Plot is used for Better Visualization of the Relationship
#### Ouput: 
# ![image](https://github.com/user-attachments/assets/ce7ed88e-cce3-4a0d-befa-2e353bd95b17)
#### - The Graph Above shows that the song 'Blinding Lights' by The Weekend got the Most streamed

### Top 5 most frequent Artists based on the Number of Tracks
#### Input:
# ![image](https://github.com/user-attachments/assets/73e37ada-c706-489a-a08f-20b613a2fc0f)
#### - The code counts the number of tracks for each artist in the artist(s)_name column, which is a data frame named df. It then counts the number of times each artist name appears with pandas by using value_counts, grabs 5 artists who have more tracks up to a maximum track overall artists and resets the index so that we get the final clean data frame
#### Output:
# ![image](https://github.com/user-attachments/assets/f6c817e7-04b4-443e-957d-1ce07b4048da)

### Graph for the Top 5 Frequent Artists
#### Input: 
# ![image](https://github.com/user-attachments/assets/142406c5-f413-467a-855e-0cdb67c9b682)
#### - Bar Plot is used for better Visualization
#### Output:
# ![image](https://github.com/user-attachments/assets/373a2d34-cc57-477a-bbe7-d5fdb9d107ab)
#### - Based on the Graph above, we can see that Taylor Swift has the highest Tracks

## Temporal Trends
### Trends in the Number of Tracks Released Over Time.
#### Input:
# ![image](https://github.com/user-attachments/assets/05d97702-d1cc-4214-9220-e439048369af)
#### The code counts the number of songs that are released annually in the DataFrame df's released_year column. The counts are obtained using value_counts(), the results are sorted by year using sort_index(), and the index is reset to generate a new data frame. Released_year, which identifies each year, and track_count, which indicates the number of tracks released in that year, are the two columns in the resulting DataFrame, track. For simpler access to the data, the code lastly sets the released_year as the DataFrame's index.
#### Sample Output:
# ![image](https://github.com/user-attachments/assets/ff863aa4-d899-4d1b-b1f3-731a18582174)

### Graph Number of Tracks Released over the Years
#### Input:
# ![image](https://github.com/user-attachments/assets/3c2147c6-b241-4498-bf5a-a1844bbe4ea0)
#### - It is the Relationship Between the Tracks over the Years
#### - Line Graph is used for better Visualization
#### Output:
# ![image](https://github.com/user-attachments/assets/fc2dd66c-7fc2-4153-b4af-1d4b4384b17c)

### Number of Tracks Released per Month
#### Input:
# ![image](https://github.com/user-attachments/assets/a485b375-6872-45c0-8f06-91ff35721772)
#### - The code called frequency.counts() takes out a frequency of release by grouping the DataFrame df in terms of the number of releases in the column called ‘released_month.’ For each value in the released_month column, there is a new separate group that uses the group by attribute.
#### Output:
# ![image](https://github.com/user-attachments/assets/4b724168-7279-449f-be6a-08d05bc284a7)
#### Based on the Graph, 2022 Has the highest number of Tracks Produced
#### Graph for the Tracks per Month
#### Input:
# ![image](https://github.com/user-attachments/assets/a4b4d483-d63f-49ad-b835-3f6a63999dc1)
#### - The text part of the code indicates the number of tracks released each month as a bar chart. It starts with an initializing of a list of months”, which is a list of twelve months in a year. This list is hence used to create a Pandas Series x which essentially becomes the x-axis labels of the bar chart. The code also sorts the DataFrame df by the released_month column and counts the number of times each month will occur using groupby() and count() before converting to a list using tolist() to form the y-axis values, y.
#### - Bargraph is used for better visualization of the relationship between the tracks  and the Months

#### Output: 
# ![image](https://github.com/user-attachments/assets/f5cf55b8-d5cb-41ec-982e-9be7042a110f)
#### - Based on the Output, January has the Most Produced Track

## Genre and Music Characteristics
### Correlation between Streams and Musical attributes
#### Input:
# ![image](https://github.com/user-attachments/assets/9f3cc8e8-8f74-48f4-adea-5e7c46706c7d)
#### - In the code snippet, the correlation coefficients of various musical attributes to the quantity of being a stream are found in df. It starts by defining a list called M_at which includes all attributes such as the BPM, key, mode, and various percentages in relation to danceability, valence, energy and among others, Streams. Each specified attribute is then cast to numeric format using the command pd.to_numeric with errors replaced with NaN because of the parameter errors=’coerce’. A blank dictionary say cor_res is created to store the correlation results. Further loop passes assigns all the remaining attributes in M_at excluding the last one (streams) calculate the corr coefficient with streams using the corr() method and appends with attribute name as “ vs Streams” for differentiation. Finally, the correlation results are converted into a DataFrame, cor_d, which contains two columns: ‘Attribute’, which contains names of the compared attribute and ‘Correlation Coefficient’ that contains the correlation values. The resulting DataFrame makes it easy to understand how each attribute is related to the number of streams.
#### Output:
# ![image](https://github.com/user-attachments/assets/90b9bda4-f401-4192-9016-db106a833add)

### Graph for the correlation of streams and attributes
#### Input:
# ![image](https://github.com/user-attachments/assets/46664f1c-8222-48ac-8798-5ec932ab5357)
#### - Markers = o provides Better visualization where the Stats of correlation at in terms of Streams
#### - Line Graph is used for  better visualization of relation ship and negative and positive Values it Holds

#### Output:
# ![image](https://github.com/user-attachments/assets/a798d392-5051-496f-80b9-1d5678473dff)
#### - Based on the graph it is Stated that Mode and streams has the highest correlation 

### Correlation between Danceability and Energy How about Valence and Acousticness
#### Input:
# ![image](https://github.com/user-attachments/assets/b7c441b3-6a07-458a-bcf6-09247ad5c8e4)
#### - For the shown DataFrame of music, the code calculates the correlation coefficients of certain musical features between each other. Ideal, it starts by creating a list called atib, containing the attributes for danceability, energy, valence, and acousticness. Preprocessing is also applied to turn all the five attributes to actual numeric format using the pd.to_numeric() which coverts any non-numeric value to NaN in case it can’t be converted. The code then uses corrcoef to calculate correlation between danceability and energy with the result stored in corr1 and also the correlation between valence and acousticness stored in corr2. The correlation figures are arranged in a dictionary called corres, where keys are informative and explain the kind of comparisons made. Last, the result is changed to the form of DataFrame by the name rescor and it offers the correlation coefficients of the specified musical attributes in transposed form and leads to the conclusion.

#### Output:
# ![image](https://github.com/user-attachments/assets/c4f34d1f-c356-49d5-abb6-6ec4d4c4f041)


## Platform Popularity
### Which platform seems to favor the most popular tracks
####  Input:
# ![image](https://github.com/user-attachments/assets/d4c14819-7114-4c34-a67e-a578c2489ca3)
#### - The code snippet gives the total track count of particular music platforms where ‘total’ counts total tracks in Spotify Playlists, Deezers Playlist, Apple Playlists, all listed in the DataFrame df. It then adds a total by each platform separately and stores these to count1, count2, and count3. Subsequently, a new DataFrame named plat_res is created, which contains two columns: The DSTs used are ‘platform’, in which the names of the platforms mentioned above have been listed, and ‘track_count,’ which displays the total count of instances about the stated platforms. This resulting data frame gives a simplified view and quantification of how many tracks are covered across the given music platforms.

#### Output:
# ![image](https://github.com/user-attachments/assets/2be012af-23b0-4f60-a7b9-385200afbf19)


### Graph on Which platform favor most of the Tracks
#### Input:
# ![image](https://github.com/user-attachments/assets/d31bf5db-edfd-4e57-a3e4-ad52f6e50b21)

#### - We use Barplots for better Visualization of the Graph
#### Output:
# ![image](https://github.com/user-attachments/assets/e9ff6ae4-5884-477d-bfbc-84414ccef6a6)

#### - Based on the Graph It is Clearly stated that in Spotify playlist in the one who favor Most of the Tracks

## Advanced Analysis
### Major vs. Minor
#### Input:
# ![image](https://github.com/user-attachments/assets/9506d22f-775f-4619-963f-cdc51f8b21f4)
#### - In this code, I convert the DataFrame df into groups based on the musical attributes of the key and mode to count the number of tracks in df associated with each set of key and mode attributes. The groupby() function creates groups and the groups are formed based on pairs of ‘key’ and ‘mode’, size() function gives the number of entries in the particular group. This count is then reset into a new DataFrame, with the column name as ‘track_count’ the number of tracks for each key-mode combination.

#### Output:
# ![image](https://github.com/user-attachments/assets/01bdf1f1-bc94-458a-8c81-af3a07fc9c4f)

### Graph of The Major and Minor 
#### Input:
# ![image](https://github.com/user-attachments/assets/2a249234-4bb9-462b-9b05-fd365fbe8101)
#### The autopct parameter is worth to be mentioned; it defines how the percentage in each part of a pie chart will look like. In the format string ‘%1.1f%%’ the mandade dictates that the percentage sign should follow the value of ‘percent’ that is formatted to one decimal place. This again provides a good informative impression about the diatonic representation of the track distribution in order to make it easier for the viewer to understand the percentage per key. Last, the title “Distribution of Tracks by Key” is given and the chart is generated through plt.show().
#### Output:
# ![image](https://github.com/user-attachments/assets/506a8747-572d-456e-b581-ce343fba1a48)
#### - Pie Graph for a better relationship Between The keys and The mode
#### - Based on the Graph the one that is Dominating is C# with 14% 

### Number of Major & Minor
#### Input:
# ![image](https://github.com/user-attachments/assets/ddabdec7-bfcc-4186-ae1f-63ab8f813f48)
#### - The code also summarizes the total number of tracks as presented in the key_mode_counts DataFrame for each musical mode. It employs USES the groupby() feature to segment the information according the ‘mode’ column, then it adds up the ‘track_count’ of each mode.
#### Output:
# ![image](https://github.com/user-attachments/assets/0ccb771b-56fa-4d95-9406-d9cafa65b8ca)

### Graph of Minor vs Major
#### Input: 
# ![image](https://github.com/user-attachments/assets/1857a67a-7a2a-4d64-88ac-495d20f00235)
#### - Pie graph is used for uniformly Used of the graph to the said sub-question and for better Visualization of who is more Dominant
#### Output:
# ![image](https://github.com/user-attachments/assets/f6363773-04c7-4743-ba2c-da9d73ea0312)
#### - The PieGraph shows that the dominant mode in terms of number of Tracks is Major

### Artists consistently appear in more playlists or charts
#### Input:
# ![image](https://github.com/user-attachments/assets/e0a5e56d-f171-42b2-8e44-974fbf8fcea7)
#### - The code snippet calculates the total number of tracks for each artist across multiple platforms, specifically focusing on Spotify playlists, Spotify charts, and Apple playlists. It begins by grouping the DataFrame df by the 'artist(s)_name' column and summing the counts for 'in_spotify_playlists', 'in_spotify_charts', and 'in_apple_playlists', resulting in three separate DataFrames: artist_playlist_counts, artist_chart_counts, and artist_apple_counts. These individual DataFrames are then merged into a single DataFrame, artist_counts, using the merge() function, which combines them based on the common 'artist(s)_name' column, with suffixes added for clarity. After renaming the 'in_apple_playlists' column for better understanding, the resulting DataFrame is sorted in Highest order based on the total count of tracks in Spotify playlists.
#### Output:
# ![image](https://github.com/user-attachments/assets/f09062fe-0390-4f0c-ae60-dc590413bc6e)
#### - We get A sample of top 10 Artists for all Tracks

### Graphing the Top 10 in each Category of Music (Spotify Playlist, Spotify charts, and Apple Playlist)
#### Input:
# ![image](https://github.com/user-attachments/assets/7adeeaa7-06ca-4b49-b30d-70917efd2e82)
#### - This code targets recognizing and displaying the first ten artists in terms of tracks allowed into Spotify and Apple Music playlists. It first aggregates the original DataFrame, df, by artist names in order to get the total track count for Spotify playlists, Spotify charts, and Apple playlists, using different DataFrames. These DataFrames are then merged to form the DataFrame named artist_counts, which contains the total counts of tracks from all three sources. The code then proceeds to sort these merged results in DataFrame and find the best 10 artists for each platform, producing three separate DataFrame for Spotify playlists, Spotify chart, and Apple playlists. All of these DataFrames then set the index as artist names so that there are no problems with the plot.

#### - Output:
### For Spotify Playlist
# ![image](https://github.com/user-attachments/assets/84fdfeb8-909a-4bce-9790-a55e961a22ae)
#### - Number 1 on the Spotify Playlist is The Weekend

### For Spotify Charts
# ![image](https://github.com/user-attachments/assets/781db078-7e3a-4dbc-8f4c-346f36b8aa5f)
#### - Number 1 on the Spotify Charts is Taylor Swift

### For Apple Playlist
# ![image](https://github.com/user-attachments/assets/4e009cf2-610b-4d4a-a31f-5a62999ad014)
#### - Number 1 on the Apple Playlist is also Taylor Swift





## Revisions
#### - v1.2 Adding 'encoding='ISO-8859-1' to the read the data set this was figured out by using chatgpt
#### - v1.3 Reivions of the code in the Overview of Dataset 
#### - v1.4 Revisions on the Basic Statistics where 'Error Coerce' was added to translate the string into numeric type. This was figured out by using ChatGPT
#### - v1.5 Revision of the plots on Released_year and artist count and making it subplots instead of 1 by 1 of plots
#### - v1.6 Adding how to get the Outliers
#### - v1.7 Determining and implementing of the Code Groupby for better and less of Code in the Dataframe
#### - v1.8 Implementing pd.tonumeric function for less of code and putting Markers on the Line Graph
#### - v1.9 Adding  and determining  the use autopct for better visualization of the Pie Graph
#### - v2.1 Adding startangle function to the pie graph for better visualization for the Pie Graph 
#### - v2.2 Utilizing the subplots and list to retrieve every top in each Data set
#### - v2.3 Making changes to the Popularity of the charts

## References/Materials Utilized:
#### - OpenAI. (2024). ChatGPT [Large language model]. https://chatgpt.com
#### - https://github.com/jonathannnpstl/top-spotify-songs-2023-EDA/blob/main/top_spotify_songs_eda.ipynb



