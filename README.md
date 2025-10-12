# Spotify and YouTube Data Analysis

This project analyzes a dataset of popular songs, combining data from both Spotify and YouTube to uncover trends in music popularity, artist performance, and song characteristics. The analysis explores relationships between Spotify streams, YouTube views, likes, comments, and various audio features.

## Dataset

The dataset used in this analysis is `Spotify_YouTube_Dataset.csv`. It contains information about thousands of popular tracks and includes the following key features:

  - **Track Information:** `Track`, `Artist`, `Album`, `Album_type`
  - **Spotify Data:** `Url_spotify`, `Stream`, and audio features like `Danceability`, `Energy`, `Acousticness`, `Loudness`, etc.
  - **YouTube Data:** `Url_youtube`, `Title`, `Channel`, `Views`, `Likes`, `Comments`, `Licensed`, and `official_video`.

## Data Cleaning and Preprocessing

Before analysis, the data was cleaned and preprocessed to ensure accuracy and consistency. The key steps included:

1.  **Removing Unnecessary Columns:** Dropped columns like `Url_spotify`, `Uri`, and `Url_youtube` that were not required for the analysis.
2.  **Handling Missing Values:**
      - Filled `NaN` values in the `Likes` and `Comments` columns with `0`, assuming that missing values indicated no likes or comments.
      - Dropped all other rows with `NaN` values to maintain the integrity of the dataset for analysis.

## Exploratory Data Analysis (EDA)

The analysis focused on answering several key questions about music popularity on both platforms.

### Top Artists and Tracks 

  - **Top 10 Artists by YouTube Views:** Identified the artists with the highest total views on YouTube.
  - **Top 10 Tracks by Spotify Streams:** Found the most streamed tracks on Spotify to understand song popularity.

### Album Analysis 

  - **Most Common Album Types:** Visualized the distribution of album types (`album`, `single`, `compilation`) in a pie chart to see which format is most prevalent.
  - **Engagement by Album Type:** Compared the average `Views`, `Likes`, and `Comments` for each album type to understand how engagement differs across formats.

### YouTube Channel Performance 

  - **Top 5 YouTube Channels by Views:** Determined the most viewed channels, which are often the official artist channels or major music labels.
  - **Likes-to-Views Ratio:**
      - Calculated the likes-to-views ratio (`LV_ratio`) to measure audience engagement.
      - Identified the top 7 tracks with the **highest** and **lowest** `LV_ratio`.

### Correlation Analysis 

A correlation heatmap was generated to visualize the relationships between key metrics: `Views`, `Likes`, `Comments`, and `Stream`. This helped understand how popularity on one platform might relate to another.

## Key Findings

  - **Strong Positive Correlation:** There is a strong positive correlation between YouTube **Views** and **Likes** (0.89), suggesting that popular videos also tend to be well-liked.
  - **Streams vs. Views:** A moderate positive correlation (0.60) exists between Spotify **Streams** and YouTube **Views**, indicating that popularity often translates across both platforms.
  - **Album Dominance:** Full-length **albums** are the most common release format, making up the majority of the tracks in the dataset.
  - **Top Performers:** Artists like Ed Sheeran, CoComelon, and channels like T-Series dominate the top charts for YouTube views, showcasing their massive global reach.

## Technologies Used

  - **Python**
  - **Pandas:** For data manipulation and analysis.
  - **NumPy:** For numerical operations.
  - **Matplotlib & Seaborn:** For data visualization.
