
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
