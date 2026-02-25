## Airbnb Price Analysis & Classification (NYC)

This project explores the Airbnb Open Data from New York City, moving from basic exploratory data analysis to implementing Machine Learning models that predict and classify listing prices.
## Project Overview

The primary goal was to identify the key factors that drive the pricing of NYC Airbnb listings. The project evolved through several stages:

    Exploratory Data Analysis (EDA): Understanding price distributions across boroughs.

    Regression Modeling: Attempting to predict exact prices.

    Classification Modeling: Categorizing listings into "Low", "Medium", and "High" price brackets for better predictive stability.

## Dataset Features

The dataset includes diverse features used to train the models:

    Location: Neighbourhood group (Manhattan, Brooklyn, Queens, etc.).

    Property Details: Room type, minimum nights, and availability.

    Host & Reviews: Number of reviews, reviews per month, and host listing count.

    Target: price (Regression) and price_category (Classification).

## Data Preprocessing

    Cleaning: Cleaned currency strings (e.g., removing $ and ,) and converted them to numerical formats.

    Feature Engineering: * One-hot encoding for categorical variables (room type, neighbourhood group).

        Created binary features like has_review.

        Handled missing values using median/mode imputation.

    Leakage Prevention: Removed the service fee column, as it showed a 1:1 correlation with the price.

## Models & Performance
1. Linear Regression (Baseline)

    Result: R2 score near 0.

    Insight: The relationship between features and price is highly non-linear in real-world NYC data.

2. Random Forest Regressor

    Result: R2 score improved to ~0.30.

    Insight: Ensemble methods captured complex patterns that linear models missed.

3. Random Forest Classifier (Final Approach)

    Approach: Discretized the price into 3 balanced quantiles: Low, Medium, and High.

    Result: Achieved an Accuracy of 53%.

    Insight: Classification proved more robust for this dataset, providing actionable insights into price "tiers".

## Key Insights

Based on the Feature Importance analysis:

    Popularity & Activity: reviews per month and availability 365 were the strongest predictors of price categories.

    Operational Rules: minimum nights significantly influenced the price tiering.

    Location vs. Management: Interestingly, how a listing is managed (availability/reviews) had a higher predictive weight than its specific location in this dataset.
