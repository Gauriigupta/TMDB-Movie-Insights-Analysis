# TMDB Movie Insights: Exploratory Data Analysis 🎬

## 📌 Project Overview
This project performs an in-depth **Exploratory Data Analysis (EDA)** on the TMDB (The Movie Database) dataset, containing information on 10,000+ movies from 1960 to 2015. The goal is to uncover the factors that contribute to a movie's success, focusing on the relationship between budget, revenue, popularity, and genres.

## 🚀 Key Business Questions
As a Data Analyst, I sought to answer:
1.  **Revenue vs. Popularity:** Does a movie’s popularity directly translate to high box-office returns?
2.  **Genre Trends:** Which genres dominate the industry in terms of production volume?
3.  **Investment Impact:** Is there a statistically significant correlation between production budget and final revenue?

## 🛠️ Tech Stack
* **Language:** Python 3
* **Libraries:** Pandas (Data Wrangling), NumPy (Numerical Analysis), Matplotlib & Seaborn (Data Visualization)
* **Environment:** Jupyter Notebook

## 🧹 Data Cleaning Workflow (The "Wrangling" Phase)
To ensure data integrity, the following steps were taken:
* **Duplicate Removal:** Identified and dropped duplicate entries.
* **Feature Selection:** Dropped irrelevant columns (e.g., `homepage`, `tagline`) to focus on key analytical variables.
* **Missing Value Treatment:** Handled null values in `cast`, `director`, and `genres` to prevent skewed results.
* **Feature Engineering:** * Created a `profit` column: $profit = revenue - budget$.
    * Cast `release_date` to datetime objects for time-series consistency.
    * Categorized `vote_average` into discrete buckets for better comparative analysis.

## 📊 Strategic Insights
* **Popularity is Profitable:** There is a clear upward trend showing that high popularity scores are strong indicators of high revenue.
* **Genre Leadership:** **Drama** is the most filmed genre (22.6%), followed by **Comedy** and **Action**, indicating these are "safer" bets for production houses.
* **Budget Correlation:** A strong positive correlation exists between budget and revenue, though outliers exist—proving that high-budget films usually earn more, but "indie" hits can still break the trend.

## 💡 Interview Talk Tracks
* **"How did you handle the pipe-separated values in genres?"**
    * *Answer:* I used string splitting techniques to isolate individual genres, ensuring each movie was counted correctly across all its associated categories.
* **"What was your biggest challenge?"**
    * *Answer:* Handling the inflation-adjusted columns (`budget_adj` and `revenue_adj`) to ensure that comparisons between a 1960s film and a 2015 film were "apples-to-apples."

---


# TMDB Movies Dataset Analysis 


| Contents 											 	   	|
| -------- 											 	   	|
| [Dataset Description](#Dataset-Description)			   	|
| [Columns Descreption](#Columns-Descreption) 		   		|
| [Questions for Analysis](#Questions-for-Analysis)	   		|
| [Data Wrangling](#Data-Wrangling)					   		|
| [Data Cleaning](#Data-Cleaning)						   	|
| [Exploratory Data Analysis](#Exploratory-Data-Analysis)	|
| [Built with](#Built-with)							   		|

## Dataset Description: 
This data set contains information about 10,000 movies extracted from [TMDB](https://www.themoviedb.org/). The dataset contains movies from 1960 to 2023. Including user ratings and revenue. Original data from [Kaggle](https://www.kaggle.com/tmdb/tmdb-movie-metadata)

## Columns Descreption:
- `id, imdb_id`: unique id or imdb id for each movie on TMDB
- `popularity`: a metric used to measure the popularity of the movie.
- `budget`:the total budget of the moviein USD.
- `revenue`:the total revenue of the movie in USD.
- `original_title`: the original title of the movie.
- `cast`:the names of the cast of the movie separated by "|".
- `homepage`: the website of the movie (if it existed).
- `director`:name(s) of the director(s) of the movie (separated by "|" if there are more than one director).
- `tagline`:a catchphrase describing the movie.
- `keywords`: keywords related to the movie.
- `overview`:summary of the plot of the movie.
- `runtime`:total runtime of the movie in minutes.
- `genres`: genres of the movie separated by "|".
- `production_companies`:production compan(y/ies) of the movie.
- `release_date`:release date of the movie.
- `vote_count`:number of voters of te movie.
- `vote_average`:the average user rating of the movie
- `release_year`:release year of the movie (from 1960 to 2015)
- `budget_adj`:the total budget of the moviein USD in terms of 2010 dollars, accounting for inflation over time.
- `revenue_adj`:the total budget of the movie in USD in terms of 2010 dollars, accounting for inflation over time.

## Questions for Analysis:
- Do movies with high popularity achive high revenvue?
- What are the most filmed genres in this whole dataset?
- Is there a correlation between a movie budget and its revenue?

## Data Wrangling:
Our data can be found on `tmdb-movies.csv` file provided on this repository. It is an edited version of the original Kaggle's [TMDB 5000 Movie Dataset](https://www.kaggle.com/tmdb/tmdb-movie-metadata) provided by Udacity on the Become a Data Analyst Nanodegree Program. 

## Data Cleaning:
**Main Observations:**
1. Our dataset consisted of a total of 10866 rows and 21 columns.
2. We had only 1 duplicated row which had been dropped.
3. Some columns wont be useful in answering our questions so they were dropped.
4. Few columns had many missing values that needed to be handled.
5. Columns `cast` `director` `genre` had values saperated with a '|'.
6. `release_date`'s data type needed to be casted.
7. We could append a column for the movie `profit` using the formula: $profit = revenue - budget$.
8. `vote_average` better be presented as a catecorical variable that groubs multible ratings values.
9. We might also catigorize `profit` column for better EDA

## Exploratory Data Analysis:
After finishing our dataset cleaning, we endded up with a total of 10840 records and 10 columns. The dataset now has no duplicates nor null values, and the data types are consistant with suitable categorical variable to address our questions.
We then perfomed some analytics and created some visualizations to answer our targeted questions.
### Q1: Do movies with high popularity achive high revenvue?
> More popular movies recieve way more revenue than the less popular movies.

### Q2: What are the most filmed genres in this whole dataset?
> - `Drama`, `Comedy` and `Action` are the most three filmed genres in total of 10839 movies in our dataset.
> - `Drama` genre alone is filmed 22.6% of the times on our dataset.

### Q3: Is there a correlation between a movie budget and its revenue?
> There is positive correlation between `budget` and `revenue`, indecating a relation between them with little outliers found. 

## Built with:
- JupyterLab
- Python3
- Pandas
- Numpy

