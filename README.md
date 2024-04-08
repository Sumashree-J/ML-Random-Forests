# ML-Random-Forests

<div align="justify"> 
    
This notebook aims to predict the Estimated_Shares_Outstanding by assessing the impact of various features in the dataset using random forests, as well as to predict whether a cell is malignant (M) or benign (B) based on its dimensions, employing decision trees.

Let's first understand these methodologies:

**Random Forests:**
Random forests select a random subset of features and uses bootstrapping techniques to choose from a list of strong learners, subsequently averaging the results of all the best trees. The construction of these trees is done parallely, making the model efficient & scalable.This approach addresses overfitting and is considered a superior estimator compared to decision trees.

**Decision Trees:**
The dataset is successively partitioned into nonoverlapping (disjoint sets), smaller datasets until each set only contains examples of the same class
An important concern here is over fitting. To prevent this, the growing step is usually followed by a pruning round which attempts to simplify the tree

**Steps:**

**Data Preparation:**
- The notebook begins by importing necessary libraries and loading the dataset, followed by renaming the columns to adhere to Python function naming conventions.
- Train-test Split: The dataset is divided into 70% for training and 30% for testing, with setting a random_state for reproducibility of the results.

**Model Development:**

Hyperparameter Tuning:
This involves adjusting parameters by explicitly specifying them in the model. Tuning is crucial as it influences how the random forest is constructed, significantly impacting its performance. Parameters like n_estimators (number of decision trees in the forest) and min_samples_split (minimum number of samples required at a leaf node) are tuned to optimize performance.

Permutation Feature Importance:
This metric measures the contribution of individual features to the model's performance by randomly rearranging data points within each feature and computing the evaluation metric. However, issues may arise when features are correlated, leading to lower reported importance values.

Mean Decrease Impurity:
This quantifies the total decrease in node impurity, providing insights into feature importance.

**Model Evaluation:**
On comparison of MSE of Random Forests & Lasso regression, results clearly show that the random forests are performing better on SEC filings data , as the model has low MSE

**Contributions:**
Feel free to submit pull requests or raise issues if you encounter bugs or have suggestions for improving this notebook. Your contributions are valued.

</div>
