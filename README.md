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
