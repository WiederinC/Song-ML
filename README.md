Song Success Predictor
======================

Overview
--------

This project is an advanced machine learning tool designed to predict the potential success of songs in the music industry. By analyzing various factors such as artist popularity, musical features, and genre, it provides insights to help record labels optimize resource allocation, enhance marketing strategies, and mitigate financial risks.

Technical Details
-----------------

### Core Algorithm

The project utilizes the **CatBoost algorithm**, known for its reliability and precision. CatBoost iteratively constructs multiple trees, refining predictions based on the errors of preceding iterations, resulting in a robust predictive model.

### Dataset

-   **Scope:** Comprehensive dataset covering the most successful songs since 2000.
-   **Features:** Includes artist popularity, musical features, genre, and additional engineered features like average popularity per genre.

### Data Preprocessing

-   **Null Values:** Removed the single data observation containing null values.
-   **Feature Selection:** Excluded non-relevant features such as `Track Name`, `Album`, and `Artist Name`.
-   **Categorical Transformation:** Transformed the `Key` feature into a binary table.
-   **Additional Features:** Added average popularity per genre and a random feature for better explainability.

### Genre Classification

-   **Approach:** Used Naive Bayes multiclass classifier to map subgenres to main genres.
-   **Benefits:** Improved sample size, reduced noise, and enhanced data accuracy.

### Popularity Binning

Experimented with different binning strategies:

-   **Mean Binning**
-   **3-Quantiles**
-   **4-Quantiles**
-   **Decision Tree Binning** (most accurate)

### Model Performance

Tested various models to find the best fit:

-   **Decision Tree**
-   **Bagging**
-   **Random Forest**
-   **K-Nearest Neighbors (KNN)**
-   **CatBoost** (top performer)

### Evaluation Metrics

Focused on metrics beyond accuracy, such as F1-score and ROC AUC, to address dataset imbalances and ensure reliable prediction of song success.

### Feature Importance

Used SHAP summary plots to understand individual feature influence, enhancing the recommendation system for artists and producers.

Conclusion
----------

This project represents a significant advancement in predicting song success, providing data-driven insights to make informed decisions. By leveraging state-of-the-art machine learning techniques and a rich dataset, it aims to revolutionize the music industry's approach to identifying potential hits.

* * * * *

Feel free to explore the code repository for detailed implementation and further technical specifics.
