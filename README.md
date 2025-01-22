# Game Recommendation System on Steam 

## Overview
A game recommendation system created for steam, a well-known video game distribution platform, is presented in this project. The system seeks to improve user engagement and happiness by offering precise and tailored game suggestions by utilizing both content-based filtering and collaborative filtering.


## Features
* ## Content-Based Filtering:
  Uses methods like Cosine Similarities and TF-IDF vectorization to analyze game metadata (titles, descriptions and genres) and suggest games that are related to user's interest.

* ## Collaborative Filtering:
  Makes game recommendation by applying the SVD algorithm to matrix factorization and user-item interaction patterns.

* ## Visualization Tools:
  Uses visual aids like boxplots, scatter plots, and heatmaps to examine the connections between attributes like pricing, user rating and positive ratios.


## Dataset
Preprocessed two sizable datasets that were taken from Steam's public repository and combined them into a single, smaller dataset that has the following characterstics: 
* app_id, user_id, title, rating, postivie_ratio, user_reviews, price, discount, platform, release_date.
* Key features from modeling: positive_ratio, id_recommendation, user_review.

## Data Preprocessing
  ## 1. Handling Missing Values:
  Removed entries with incomplete or invalid data (e.g., missing ratings or titles).

  ## 2. Feature Encoding:
  Categorical attributes such as "platform" and "is_recommended" were label-encoded for compatibility with numerical operations.

  ## 3. Feature Scaling:
  Applied Min-Max normalization to columns like "price" and "positive_ratio" for uniform scaling.

  ## 4. Text Processing:
  Normalized game titles using TF-IDF, addressing punctuation and case sensitivity.

## Methodology
  ## 1. Content-Based Filtering:
  * ## TF-IDF Vectorization:
    Extracted textual features from game titles and descriptions.
  * ## Cosine Similarity:
    Used to compute the closeness between games and recommend similar titles.

      ## Example:
      A query for "Grand Theft Auto IV" returned:
        * "Grand Theft Auto 2"
        * "Grand Theft Auto V"
        * "Grand Theft Auto: Episodes from Liberty City"
        * "Nioh 2: The Complete Edition"
        * "Nioh: The Complete Edition"
      The average precision achieved for content-based recommendations was 0.78.
  ## 2. Collaborative Filtering:
  * ## SVD (Singular Value Decomposition):
    Used in the user-item interaction matrix for matrix factorization in order to forecast missing ratings.
  * ## Evaluation Metric:
    Root Mean Square Error (RMSE) was used for validation, and the average test score was 0.329.

## Technologies Used
- Python
- Surprise Library
- Scikit-learn 
- Matplotlib/Seaborn
- Google Colab
- NumPy
- Pandas

## How to Run
  ## 1. Clone repository:
    git clone https://github.com/mearnav/Data_Mining_Project
    cd Data_Mining_Project
  ## 2. Install dependencies:
    pip install -r requirements.txt
  ## 3. Execute the script:
    python main.py

## Results and Visualizations
  ## 1. Content-Based Filtering:
  Successfully provided accurate and thematic recommendations for diverse game genres.
  ## 2. Collaborative Filtering:
  Demonstrated robust performance in uncovering user preferences and recommending games within subgenres of interest.
  ## 3. Visualization Highlights:
   * ## Boxplots:
   Showed the correlation between "positive_ratio" and game ratings.
   * ## Scatter Plots:
   Explored pricing trends relative to user reviews and ratings.
   * ## Heatmaps:
   Visualized user-item interaction scores in collaborative filtering.
