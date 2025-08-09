Restaurant Data Analysis & Modeling: Internship Project

Project Overview
This repository documents a series of data science tasks completed during an internship @Cognifyz Technologies, focused on analyzing a comprehensive restaurant dataset. The project explores three key areas:
Task 1: Predictive Modeling of Restaurant Ratings: Building regression models to predict a restaurant's aggregate rating.
Task 2: Content-Based Recommendation System: Developing a system to recommend similar restaurants based on their attributes.
Task 3: Cuisine Classification: Attempting to classify the primary cuisine of a restaurant, highlighting the challenges of multi-class classification with imbalanced data.

Dataset
All tasks utilize the same restaurant dataset given by the company.
Key features include:
Restaurant Info: Restaurant Name, Cuisines, City, Locality.
Pricing & Services: Average Cost for two, Price range, Has Table booking, Has Online delivery.
Ratings: Aggregate rating, Rating text, Votes.

Tasks and Methodology

Task 1: Predictive Modeling of Restaurant Ratings
Objective: To predict the Aggregate rating of a restaurant based on its features.

Methodology:
Preprocessing: Handled missing values and performed one-hot encoding on categorical features like Has Table booking and Has Online delivery.
Feature Engineering: Selected relevant features for prediction.

Modeling: Trained and evaluated two regression models:
Linear Regression
Random Forest Regressor

Evaluation: Compared models using R² score, Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE).

Findings:
The Random Forest Regressor significantly outperformed the Linear Regression model.
It achieved a much higher R² score and lower error metrics, indicating it was a more accurate and reliable model for predicting restaurant ratings.

Task 2: Content-Based Restaurant Recommendation System

Objective: To build a system that recommends similar restaurants to a user based on a selected restaurant.

Methodology:
Feature Selection: Used Cuisines, Price range and Aggregate rating as the core attributes for comparison.
Feature Combination: Merged these selected attributes into a single text string for each restaurant.
Vectorization: Applied the TF-IDF (Term Frequency-Inverse Document Frequency) technique to convert the combined text features into numerical vectors.
Similarity Calculation: Used Cosine Similarity to measure the similarity between the TF-IDF vectors of different restaurants.
Recommendation Function: Implemented a function that takes a restaurant name as input and returns a list of the most similar restaurants.

Findings:
The content-based filtering approach was successful.
The system effectively recommended restaurants with similar cuisines, price levels, and ratings, demonstrating its ability to make relevant suggestions based on item attributes alone.

Task 3: Cuisine Type Classification

Objective: To predict a restaurant's cuisine type from its other features, exploring a multi-class classification problem.

Problem Framing: The Cuisines column was treated as the target variable. Due to the high number of unique cuisines, the problem was framed as a multi-class classification task.

Modeling: Trained and evaluated two classification models:
Logistic Regression
Random Forest Classifier
Evaluation: Assessed model performance using classification reports and confusion matrices.

Findings & Challenges:
Both models struggled to perform well, particularly the Logistic Regression model.
Class Imbalance: The primary challenge was the severe class imbalance in the dataset. A few cuisines (like North Indian, Chinese) were extremely common, while most others were rare.
The models were biased towards predicting the most frequent classes and failed to correctly classify the underrepresented ones. This task served as an important case study on the limitations of standard classification models on highly imbalanced, multi-class data.

Overall Conclusion
This internship project provided hands-on experience across a range of machine learning tasks. The Random Forest algorithm proved to be a versatile and powerful tool for both regression (Task 1) and classification. The recommendation system (Task 2) demonstrated the effectiveness of content-based filtering. Finally, the classification task (Task 3) was a valuable lesson in the practical challenges of dealing with real-world, imbalanced data.
