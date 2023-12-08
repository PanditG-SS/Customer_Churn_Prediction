# Customer_Churn_Prediction 

1. **Data Loading and Exploration:**
   - The dataset is loaded from a CSV file using pandas (`pd.read_csv`).
   - The 'customerID' column is dropped, as it's not required for the analysis.
   - The data types of columns are printed, and the shape of the DataFrame is displayed.

2. **Data Cleaning and Preprocessing:**
   - Rows with 'TotalCharges' equal to ' ' are removed, and the 'TotalCharges' column is converted to numeric.
   - Bar graphs are created to visualize the relationship between tenure and customer churn.

3. **Data Transformation:**
   - Categorical variables are converted to numerical format:
     - 'No internet service' and 'No phone service' are replaced with 'No'.
     - 'Gender' is converted to binary (0 for Male, 1 for Female).
     - Columns with 'Yes' and 'No' values are replaced with 1s and 0s.

4. **Dummy Variable Creation:**
   - Dummy variables are created for categorical columns like 'InternetService', 'Contract', and 'PaymentMethod' using `pd.get_dummies`.

5. **Data Scaling:**
   - Some columns ('tenure', 'MonthlyCharges', 'TotalCharges') are scaled using `MinMaxScaler`.

6. **Train-Test Split:**
   - The data is split into training and testing sets using `train_test_split`.

7. **Neural Network Model:**
   - A neural network model is defined using Keras with one hidden layer containing 20 neurons and an output layer with one neuron using a sigmoid activation function.
   - The model is compiled with binary crossentropy loss and the Adam optimizer.

8. **Training:**
   - The model is trained on the training set for 100 epochs.

9. **Evaluation:**
   - The model is evaluated on the test set, and the results are printed.
   - Predictions are made on the test set, and a classification report is generated using `sklearn.metrics.classification_report`.
   - A confusion matrix is created and visualized using `seaborn.heatmap`.

10. **Conclusion:**
    - The model's performance is evaluated based on metrics such as accuracy, precision, recall, and F1-score.
    - The confusion matrix provides insights into true positive, true negative, false positive, and false negative predictions.

It's important to note that the choice of the neural network architecture and hyperparameters can significantly impact the model's performance.

|           | Precision | Recall | F1-Score | Support |
|-----------|-----------|--------|----------|---------|
| **0.0**   | 0.83      | 0.89   | 0.86     | 999     |
| **1.0**   | 0.67      | 0.54   | 0.60     | 408     |

# Accuracy for the Model from Confusion Matrix.
# 79%

