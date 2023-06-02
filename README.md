## Prediction of Car Prices

## Objective
The project objective is to develop a predictive model that can accurately estimate car prices in England by leveraging on historical data (provided by Auto Trader) on car attributes, such as make, model, year, mileage, condition, and other relevant factors, to build a model capable of predicting the prices of cars in the market.

By addressing this problem, the aim is to provide valuable insights and assistance to car buyers, sellers, and market participants in making informed decisions regarding car purchases, valuations, and negotiations in the dynamic automotive market in England.

## Project Approach
Data Preprocessing: Clean and preprocess the data, identify and deal missing values using pipelines and simple Imputer, outliers, noises to ensure data quality and reliability.

## Feature Engineering and selection:
Engineered new features from the existing ones, including computing car age, grouping infrequent values of categrorical features, Clusters, and polynomial features to second degree. In addition to this, used KBest to automatically select features as part of our predictors and recursively eliminated least important features using RFECV

## Model Selection and Training:
The data was divided into training and testing sets to evaluate the models effectively. Various machine learning algorithms suitable for regression tasks, including linear regression, random forests, gradient boosting, and ridge regression, were explored. A grid search technique was employed to identify the best parameters for each model, optimizing their performance.

The selected models were respectively trained on the training data, and hyperparameters were fine-tuned to enhance performance, utilizing techniques like cross-validation to prevent overfitting. Additionally, an ensemble model was implemented to combine the predictions from all the models used, leveraging their collective insights and improving the overall predictive power.

## Model Evaluation:
The trained model was evaluated using the testing data to measure its accuracy in predicting car prices. Various evaluation metrics were computed, and the results were compared by visualizing them through dataframes and plots. The true values were compared to the predicted values using the ensemble model, which incorporated all four models and an averager. Furthermore, global and local explanations of SHAP values were computed to understand their impact on the predicted values.

Partial Dependence Plots (PDPS) were also utilized to analyze the relationship between individual features and the predicted car prices. Overall, these analyses provided insights into the model's performance, the importance of different features, and the factors influencing the predicted car prices.

Comparing all models, GRadiest Boosting regressor was the best performing model with the least Mean Absolute Error and Root Mean Squared Error
