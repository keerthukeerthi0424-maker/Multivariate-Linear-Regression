# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
<br>Import pandas and linear_model from sklearn.

### Step2
<br>Load the dataset from "carsemission.csv" into a DataFrame.

### Step3
<br>Assign 'Weight' and 'Volume' as features ($X$) and 'CO2' as the target ($y$).

### Step4
<br>Initialize the LinearRegression model and fit it with $X$ and $y$.

### Step5
<br>Print the model coefficients and intercept.

### Step6
<br>Provide new input data (Weight: 3300, Volume: 1300) to predict and print the expected CO2 emissions.

## Program:
```
Developed by: Keerthana T A
Register num: 26009041
import pandas as pd 
from sklearn import linear_model
df = pd.read_csv("carsemission.csv")
X = df[['Weight', 'Volume']]
y = df['CO2']
regr = linear_model.LinearRegression()
regr.fit(X, y)
print('Coefficients:', regr.coef_)
print('Intercept:', regr.intercept_)
input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})
predictedCO2 = regr.predict(input_data)
print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)


```
## Output:

<br><img width="843" height="465" alt="image" src="https://github.com/user-attachments/assets/d85abf43-3c6c-4344-bcb0-f1819fbc9cdc" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
