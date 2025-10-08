# Predicting-1-Bedroom-Apartment-Rental-Prices-

I'm excited to share a recent machine learning project I completed for predicting monthly rental prices for 1-bedroom apartments in various cities across the United States.

**The Problem:** Fluctuations in rental prices and the difficulty in predicting them make it challenging for individuals and businesses to make informed decisions. This project aims to build a model that can predict future rental prices based on historical data and geographical features.

**The Data:** I used a dataset containing monthly rental prices for 1-bedroom units for several US cities over a period of time, along with geographical information such as city name, state, county, and metropolitan area.

**Methodology:**
1. Data Cleaning: I handled missing values and managed outliers to ensure data quality.
2.  **Feature Engineering:** I extracted new features with high predictive value, including:
    *   Geographical distances to key reference points (like the center of the US, state capitals, Washington D.C., and the coastline).
    *   Time-series based features from historical prices (like the standard deviation and trend slope of prices over the past 19 months).
    *   Clustering regions based on geographical location using the K-Means algorithm.
3.  **Categorical Feature Handling:** I applied the advanced Target Encoding technique to transform categorical features (such as State, Metro, CountyName, and K-Means clusters) into numerical representations that capture the relationship with the target rental price, while avoiding data leakage.
4.  **Model Building:** I trained an XGBoost Regressor model, a powerful gradient boosting tree model, to predict the rental price for December 2019. I chose XGBoost for its ability to capture complex relationships in the data.
5.  **Evaluation:** I evaluated the model's performance on unseen test data using key metrics such as R-squared, RMSE, and MAE.

**Key Results:**
The model achieved excellent performance on the test data, with an R-squared of approximately 0.9879, indicating that the model explains a very large portion of the variance in rental prices. The RMSE and MAE values were also relatively low (around $61.55 and $45.24 respectively), suggesting that the model's predictions are, on average, very close to the actual prices. **This strong performance is visually demonstrated in the Actual vs. Predicted Rental Prices plot.** Feature importance analysis showed that the latest known price, geographical features, and time-series based features were the most influential in the prediction. **You can see the impact of different factors in the Feature Importance plot.**

**Conclusion:**
This project demonstrates how a combination of historical data, geographical features, and advanced machine learning techniques can be used to build a robust rental price prediction model. Although there was no explicit feature selection step, the model's performance and feature importance analysis indicate that the model effectively utilized the available features. **The influence of geographical factors, such as distance to the coast, is illustrated in the relevant plot.** **Furthermore, the variation in average rental prices across different geographical clusters is shown in the Mean Price per Cluster plot.** With more data available, this idea can be scaled to include other types of properties or wider geographical areas, increasing its accuracy and potential applications.

**Note:**
To try the model without need for running the whole nootbook upload the function file, the Kmeans model file, the target encoder file and the xgb_rental_price_model file

Happy to share the full notebook detailing all the steps [**https://colab.research.google.com/drive/1Gge82kanqp_BlmrQckiUaegqkepFEeeV?usp=sharing**].
