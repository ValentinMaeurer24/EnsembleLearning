# EnsembleLearning
## AirBnB New York Price Prediction
### Predicting Airbnb Prices in New York City using Ensemble Learning Techniques
This GitHub repository contains the code and documentation for a project that uses ensemble learning techniques to predict Airbnb prices in New York City. The project pre-processes data, applies one hot encoding, log transformation of the target variable, creates new features such as 'multi_listing', 'rentals', and performs dimensionality reduction using PCA. Various models, including Elastic Net, Decision Tree Regressor, Random Forest Regressor, XGBoost Regressor, AdaBoost Regressor, Bagging Regressor, and Stacking Regressor, are trained on the pre-processed data, and the performance of each model is evaluated using R-squared and mean absolute percentage error (MAPE) metrics.

### Data Set
The dataset used for this project has been sourced from Kaggle and comprises information on the listings in New York City in the year 2019. It encompasses 15 features of listings, which include the name of the listing, neighborhood, price, review details, and availability. The dataset consists of approximately 47,000 listings.

### Exploratory Data Analysis
The EDA section explores the dataset to gain insights into the relationships between different features. The histogram of the target variable 'price' indicates that the distribution of prices is highly skewed to the right, with the majority of listings having prices below $1000 and a few listings having prices over $10,000. The barplot of the categorical variable 'neighbourhood_group' against the target variable 'price' shows that Manhattan has the highest average price of listings, while Bronx has the lowest.

### Pre-processing
The pre-processing section performs data cleaning, including one hot encoding, log transformation of the target variable, creating new features such as 'multi_listing', 'rentals', and performing dimensionality reduction using PCA.

### Modelling
The modelling section trains various models, including Elastic Net, Decision Tree Regressor, Random Forest Regressor, XGBoost Regressor, AdaBoost Regressor, Bagging Regressor, and Stacking Regressor, on the pre-processed data. The performance of each model is evaluated using R-squared and mean absolute percentage error (MAPE) metrics.

### Conclusion
The conclusion section summarizes the findings of the project, demonstrating the effectiveness of ensemble learning techniques in predicting Airbnb prices. The XGBoost and Stacking Regressor models outperformed the other models, which are expected to improve the accuracy and reduce the variance of the base models. The project can be used by hosts to set optimal prices for their listings.

Overall, this repository provides a comprehensive guide to predicting Airbnb prices in New York City using ensemble learning techniques, with well-documented code and visualizations.






## Decision Tree Model Implementation

All of us worked on the development of the code for the decision tree. Due to its minor length, however, we decided to upload our final result all at once.

### Building the Tree

This is a decision tree model implemented in Python using NumPy library. The model can be used for both classification and regression tasks.

The decision tree model implemented here follows the standard recursive partitioning strategy. The algorithm starts by considering the entire input dataset and recursively splits the data based on the values of the input features. The splitting criterion is chosen based on the cost function, which measures the quality of the split based on the distribution of the target variable in the resulting subsets. The cost function used in this implementation can be either the Gini index for classification problems or the mean squared error for regression problems.

### Parameters

The model takes the following parameters:

    min_samples_split: The minimum number of samples required to split an internal node. The default value is 2.
    max_depth: The maximum depth of the tree. The default value is 5.
    task: The type of task the model is used for. It can be either "classification" or "regression". The default value is "classification".
    max_features: The maximum number of features to consider when looking for the best split. If None, all features will be considered. The default value is None.
    random_state: The seed value for the random number generator. The default value is None.
    
### Methods

The following methods are implemented in the model:

    fit(X, y): Fit the model to the training data (X, y).
    predict(X): Make predictions for the input data X.
    get_params(deep=True): Get the parameters of the model.
    set_params(**params): Set the parameters of the model.
    
### Node Class

The model also includes a Node class, which is used to represent each node of the decision tree. Each node has the following attributes:

    feature: The feature index used to split the data.
    threshold: The threshold value used to split the data.
    left: The left child node.
    right: The right child node.
    value: The predicted value at the node (for leaf nodes only).
    
### Splitting Criteria

The model uses two splitting criteria:

    Gini impurity (for classification tasks)
    Mean squared error (for regression tasks)
