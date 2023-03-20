# EnsembleLearning
## AirBnB New York Price Prediction







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

### Final results

#### Evaluation of the performance of our Decision Tree on the Auto MPG dataset

To evaluate our decision tree regressor's performance, we calculated its MSE and R^2 score on the Auto MPG dataset, which predicts fuel efficiency based on vehicle features.

The MSE of 22.95 suggests that while the model has learned patterns in the data and provides a reasonable approximation, there is still room for improvement as there is still some difference between the predicted fuel efficiency values and the actual values

The R^2 score of 0.5503 suggests that our decision tree model provides a reasonable approximation of fuel efficiency. The R^2 score indicates that the model can explain approximately 55.03% of the variance in the target variable.

These results demonstrate that the tuned hyperparameters min_samples_split (17), max_depth (19), and max_features (1) make the model perform relatively well on this regression task.

In conclusion, our decision tree regressor is a fairly reliable model for simple regression tasks

#### Evaluation of the performance of our Decision Tree on the Iris dataset*

To evaluate our decision tree classifier's performance, we decided to calculate its cross-validated accuracy on a classic dataset for classification (the Iris dataset).

The average accuracy score on this classification task is 96% which suggests that our decision tree performed really well and could accurately predict the species of iris flowers based on their features. 
The standard deviation of 0.025 is very low which suggests that the model is consistent in its predictions across different splits of the dataset.

These results also show that the default values we chose for min_samples_split (2), max_depth (5) and max_features (None) work perfectly well for simple classification tasks

In conclusion, the results indicate that the custom-built decision tree classifier is a reliable model for classifying iris flowers in the given dataset.
