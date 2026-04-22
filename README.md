🚗 Predicting Used Car Prices in Virginia

APMA 3150 – Group 9
Kevin Cha, Qixiang Gao, Prabhnoor Kaur

📌 Overview

This project explores the question:
What factors are most important in driving used car prices in Virginia, and can we use them to accurately predict price?

We analyze Craigslist car listing data and build multiple machine learning models to understand key price drivers and evaluate prediction performance.

📊 Dataset
Source: Kaggle (Craigslist Vehicles Dataset, 2020)
Original size: ~426,000 listings
Filtered to Virginia: 10,732 listings
After cleaning: 2,052 listings
Features used:
Year
Condition
Fuel type
Odometer
Transmission
Drive type
Region
Title status
Cylinders (with limitations)
⚙️ Data Processing
Removed null and inconsistent values
Filtered to Virginia listings only
Dropped high-cardinality/noisy columns (e.g., model)
Performed feature selection based on relevance and usability
Used an 80/20 train-test split for all models
🤖 Models Implemented
1. Random Forest
RMSE: ~$5,029
Best performing model
Most important feature: Year
2. Gradient Boosting
RMSE: ~$5,350
Slightly worse than Random Forest
Also identified Year as most important
3. Linear Regression
RMSE: ~$7,804
Used for interpretability
Key predictors: year, condition, fuel type, odometer, drive, region
📈 Key Findings

Across models, the most important factors were:

Year
Odometer (mileage)
Fuel type
Region
Car type
Cylinder count

These features consistently influenced price predictions across different modeling approaches.

⚠️ Limitations
Data comes from listings, not actual sale prices
Heavily skewed toward private sellers (Craigslist)
Some missing or inconsistent data due to scraping
Limited to Virginia → may not generalize nationally
💡 Takeaways
Newer cars and lower mileage strongly increase price
Feature engineering and data cleaning significantly impacted model performance
Ensemble models (Random Forest, Boosting) performed better than linear models
Results provide a baseline understanding, not exact market pricing
📚 References
Andrews, T., & Benzing, C. (2006). Determinants of Price in Internet Auctions of Used Cars
Reese, A. (2020). Craigslist Vehicles Dataset (Kaggle)
🚀 Future Improvements
Expand dataset beyond Virginia
Incorporate dealership data
Improve handling of categorical variables
Try more advanced models (e.g., XGBoost, neural networks)
