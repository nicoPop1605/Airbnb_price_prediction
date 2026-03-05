## Airbnb Price Analysis & Classification (NYC)

This project explores the Airbnb Open Data from New York City, moving from basic exploratory data analysis to implementing Machine Learning models that predict and classify listing prices.

## Project Overview
This project performs an end-to-end Data Science analysis on the NYC Airbnb Open Data. The primary objective is to identify the factors that drive listing prices and to build a Machine Learning model capable of classifying rentals into price categories: Cheap, Medium, and Expensive.

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

## Machine Learning
Algorithm: Random Forest Classifier.

Target: Multi-class classification (Cheap, Medium, Expensive).

Evaluation: Used Accuracy, Precision, and Recall via a Classification Report.

Feature Importance: Extracted the most influential features, revealing that Coordinates and Construction Year drive the most value.

## Key insights
Location is Granular: While general boroughs (Manhattan, Brooklyn) provide a baseline, latitude and longitude (micro-location) are much stronger predictors of price.

The Service Fee Trap: Identified a 0.99 correlation between price and service fee. Removed the fee during modeling to prevent data leakage and ensure the model learns from real attributes.

Market Distribution: The NYC market shows a surprisingly uniform distribution of prices, meaning there is a consistent supply of listings across all budget ranges ($50 to $1,200).

    Result: Achieved an Accuracy of 64%.

    Insight: Classification proved more robust for this dataset, providing actionable insights into price "tiers".

## Tech Stack
-Language: Python 3.x

-Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-Learn

-Environment: Jupyter Notebook

