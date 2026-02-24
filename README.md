# Airbnb_price_prediction

## Project Overview

This project explores price prediction for Airbnb listings using machine learning techniques.  
The objective is to understand which features influence listing prices and evaluate different regression models.

## Dataset

The dataset contains structured information about Airbnb listings, including:

- Minimum nights
- Number of reviews
- Reviews per month
- Review rating
- Availability (365 days)
- Room type
- Neighbourhood group
- Host listing count

Target variable:
- Price

## Data Preprocessing

- Removed missing values
- One-hot encoded categorical variables
- Created a binary feature (`has_review`)
- Removed `service fee` to prevent data leakage
- Split data into training and testing sets (80/20)

## Models Implemented

### Linear Regression
Used as a baseline model.  
Result: Low R² score, indicating limited linear relationship between features and price.

### Random Forest Regressor
Captured non-linear relationships and improved performance compared to Linear Regression.

## Evaluation Metrics

- Mean Squared Error (MSE)
- R² Score

## Key Insights

- Room type and neighbourhood influence price more than review-related features.
- Linear models are insufficient for complex real-world pricing patterns.
- Preventing data leakage is critical for reliable model evaluation.

## Future Improvements

- Hyperparameter tuning
- Cross-validation
- Advanced feature engineering
- Trying Gradient Boosting methods

---

*This project is part of my ongoing exploration of Machine Learning and AI systems.*
