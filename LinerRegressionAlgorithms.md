# Understanding Liner Regression Algorithms in Machine Learning

**Introduction:**

Machine learning empowers computers to discern patterns and make predictions based on data. An integral facet of machine learning is regression analysis, a set of techniques employed for forecasting a continuous outcome variable using one or more predictor variables.

**What is Regression?**

Regression is a form of "Supervised Machine Learning." It is a statistical method that seeks to establish a relationship between a 'target' and one or more independent variables (features or predictors). The objective is to construct a model capable of accurately predicting the target variable based on the given features. The output of a regression model is a continuous value, rendering it suitable for tasks such as predicting prices, sales, or any other numerical quantity.

**Liner Regression Algorithms**

Linear regression stands out as one of the simplest and most widely utilized regression algorithms. It presupposes a linear relationship between the independent and dependent variables. The model articulates this relationship with a straight line, where coefficients determine the slope and intercept.

Understanding the Linear Regression Algorithm with Sample Data:

1. Select the training data which we want to use for Liner Regression. Split the data in two sets. The first dataset is used to train the algorithm, while the second set serves for validation on the trained model.

Sample Coffee Sale Data with Temperature:

| **Temp** °C | **Coffee Sale** |
| --- | --- |
| 18 | 60 |
| 19 | 60 |
| 20 | 58 |
| 21 | 57 |
| 22 | 55 |
| 23 | 55 |
| 24 | 54 |
| 25 | 50 |
| 26 | 45 |
| 27 | 48 |
| 28 | 45 |
| 29 | 42 |
| 30 | 40 |
| 31 | 38 |
| 32 | 35 |
| 33 | 35 |
| 34 | 32 |


Split the data into training and validation datasets:

Training Dataset:

| **Temp °C** | **Coffee Sale** |
| --- | --- |
| 18 | 60 |
| 19 | 60 |
| 20 | 58 |
| 21 | 57 |
| 23 | 55 |
| 24 | 54 |
| 25 | 50 |
| 28 | 45 |
| 29 | 42 |
| 31 | 38 |
| 32 | 35 |
| 34 | 32 |

Validation Dataset

| **Temp °C** | **Coffee Sale** |
| --- | --- |
| 22 | 55 |
| 26 | 45 |
| 27 | 48 |
| 30 | 40 |
| 33 | 35 |

1. We will create Excel chart with trendline to derive the regression equation (model). In the chart you can see that we have liner regression equation which is

Y (Coffee sale) = -1.8503 x (Temperature) + 95.708

![](RackMultipart20240105-1-awqail_html_713ba6faebce41b3.gif)

1. Use the validation dataset to test the model by predicting values based on the derived formula.

Y (Coffee sale) = -1.8503 x (Temperature) + 95.708

| **Temp °C** | **Coffee Sale (Actual)** | **Coffee Sale (Predicated)** |
| --- | --- | --- |
| 22 | 55 | 55 |
| 26 | 45 | 48 |
| 27 | 48 | 46 |
| 30 | 40 | 40 |
| 33 | 35 | 35 |

1. Compare the known actual values against predicted values, calculating error and accuracy.

| **Temp °C** | **Coffee Sale (Actual)** | **Coffee Sale (Predicated)** | **Absolute Error** | **Squared Error** |
| --- | --- | --- | --- | --- |
| 22 | 55 | 55 | 0 | 0 |
| --- | --- | --- | --- | --- |
| 26 | 45 | 48 | 3 | 9 |
| --- | --- | --- | --- | --- |
| 27 | 48 | 46 | 2 | 4 |
| --- | --- | --- | --- | --- |
| 30 | 40 | 40 | 0 | 0 |
| --- | --- | --- | --- | --- |
| 33 | 35 | 35 | 0 | 0 |
| --- | --- | --- | --- | --- |
| Mean Absolute Error (MSE) | 1 |
| --- | --- |
| Mean squared error (MSE) | 2.6 |
| Root mean squared error (RMSE) | 1.61245 |
| Coefficient of determination (R2) | 0.946058 |

The Mean Absolute Error (MAE), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE) are metrics used to evaluate the performance of a regression model. Here's what each of these metrics indicates:

**Mean Absolute Error (MAE):**

MAE represents the average absolute difference between the predicted values and the actual values.

A lower MAE suggests that the model's predictions are closer to the actual values.

In our example, the MAE is 1, indicating that, on average, the model's predictions deviate by 1 unit from the actual values.

**Mean Squared Error (MSE):**

MSE calculates the average of the squared differences between the predicted and actual values.

Squaring emphasizes larger errors, making it more sensitive to outliers.

The MSE value of 2.6 in our case indicates the average squared deviation between predicted and actual values.

**Root Mean Squared Error (RMSE):**

RMSE is the square root of the MSE, providing a measure in the original units of the target variable.

Like MSE, it penalizes larger errors more heavily.

The RMSE value of 1.61245 indicates the average magnitude of the errors in the predicted values.

**Coefficient of Determination** **(****R²****)**

R² is considered as Measure of Goodness of Fit. R² provides a measure of how well the regression model fits the actual data.

A higher R² value indicates a better fit, suggesting that a larger proportion of the variance in the dependent variable is explained by the independent variables.

**Conclusion:**

The low MAE (1) suggests that, on average, your model's predictions are relatively close to the actual values.

The MSE (2.6) and RMSE (1.61245) values provide a sense of the overall accuracy, considering the squared errors. Lower values are generally desirable.

In our case, the Coefficient of Determination (R²) is 0.946058, which suggests that approximately 94.6% of the variability in coffee sales can be explained by the linear regression model based on temperature. This is a strong indication of the model's effectiveness in explaining the observed patterns in the data.

In summary, based on these metrics, our linear regression model appears to perform well on the given dataset, with predictions close to the actual values. However, it's crucial to interpret these metrics in the context of the specific problem and dataset.
