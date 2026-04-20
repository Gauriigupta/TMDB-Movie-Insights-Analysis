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
