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
- Keras

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

## Limitations
  ## 1. Scalability:
  Real-time applicability for large datasets is limited by memory-intensive similarity calculations in both methods.
  ## 2. Dynamic Preferences:
  It is necessary to regularly retrain for relevance as user preferences change.
  ## 3. Query Handling:
  Errors such as typos or unclear inputs cam impact the accuracy of recommendations.

## Future Improvements
  ## 1. Enhanced Personalization:
  * Incorporate user reviews and sentiment analysis for richer insights.
  * Explore additional game metadata like developers, genres and gameplay mechanics.
  ## 2. Real-Time Recommendations:
  * Create a dynamic recommendation engine that will be updated when users engage with the system.
  ## 3. Scalability:
  * To manage big datasets effictively, use distributed computing or approximate closest neighbor methods.

## References
  * Bogers, T. and Van den Bosch, A., 2009. Collaborative and content-based filtering for item recommendation on social bookmarking websites. Submitted to CIKM, 9.
  * Aggarwal, P., Tomar, V. and Kathuria, A., 2017. Comparing content based and collaborative filtering in recommender systems. International Journal of New Technology and Research, 3(4), p.263309.
  * Javed, U., Shaukat, K., Hameed, I.A., Iqbal, F., Alam, T.M. and Luo, S., 2021. A review of content-based and context-based recommendation systems. international Journal of Emerging Technologies in Learning       (iJET), 16(3), pp.274-306.
  * Fu, L. and Ma, X., 2021. An improved recommendation method based on content filtering and collaborative filtering. Complexity, 2021(1), p.5589285.
  * Claypool, M., Gokhale, A., Miranda, T., Murnikoc, P., Netes, D. and Sartin, M., 1999, August. Combining content-based and collaborative filters in an online newspaper. In Proceedings of ACM SIGIR workshop on recommender systems (Vol. 60, pp. 1853-1870).
  * Kim, B.D. and Kim, S.O., 2001. A new recommender system to combine content-based and collaborative filtering systems. Journal of Database Marketing & Customer Strategy Management, 8, pp.244-252.
