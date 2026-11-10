
# AI/ML Learning Project

## Feature Scaling

Feature Scaling converts numerical features
into a comparable scale.

### 1. Normalization (Min-Max Scaling)

- Converts values into a range of 0 to 1.
- Uses MinMaxScaler.

### 2. Standardization

- Scales data around mean 0 and standard deviation 1.
- Uses StandardScaler.
\n## MinMaxScaler Practical\n\n### Python Code\n```python\n
from sklearn.preprocessing import MinMaxScaler
import pandas as pd

data = {'Age': [10, 20, 30]}
df = pd.DataFrame(data)

scaler = MinMaxScaler()
scaled_data = scaler.fit_transform(df)

print(scaled_data)
\n```\n\n### Output\n```text\n
[[0. ]
 [0.5]
 [1. ]]
\n```\n\n## StandardScaler Practical\n\n### Python Code\n```python\n
import pandas as pd
from sklearn.preprocessing import StandardScaler

data = {
    'Age': [10, 20, 40, 50]
}

df = pd.DataFrame(data)

scaler = StandardScaler()
scaled_data = scaler.fit_transform(df)

print(scaled_data)
\n```\n\n### Output\n```text\n
[[-1.2649]
 [-0.6325]
 [ 0.6325]
 [ 1.2649]]
\n```\n

## Comparison: MinMaxScaler vs StandardScaler

| MinMaxScaler | StandardScaler |
|---|---|
| Performs Normalization | Performs Standardization |
| Uses minimum and maximum | Uses mean and standard deviation |
| Values usually range from 0 to 1 | Mean becomes 0 and SD becomes 1 |
| Sensitive to outliers | Also affected by outliers |

## Conclusion

Feature Scaling helps bring numerical features
to a comparable scale.

MinMaxScaler is useful when a fixed range is needed.
StandardScaler is useful when data needs to be
centered around mean 0 with standard deviation 1.

## Linear Regression

Linear Regression is a supervised machine learning algorithm used to predict continuous numerical values.

### Dataset
- Input Feature (X): Study Hours
- Target (y): Marks

### Steps Performed
1. Created a dataset using Pandas.
2. Separated input and target variables.
3. Split data into training and testing sets.
4. Trained a Linear Regression model.
5. Predicted marks using test data.
6. Evaluated the model using Mean Absolute Error (MAE).
7. Calculated Slope and Intercept.
8. Visualized the regression line using Matplotlib.

### Linear Regression Equation

y = mx + c

For this practical:

y = 10x + 20

### Libraries Used
- Pandas
- Scikit-learn
- Matplotlib

### Practical Notebook
`Linear_Regression_Practical.ipynb`

