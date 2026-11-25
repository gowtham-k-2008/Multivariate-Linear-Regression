# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
<br> Import Load Dataset.

### Step2
<br>Define features and target.

### Step3
<br> Initialize and train the model.

### Step4
<br> Extract model parameters.

### Step5
<br> Predict and display output.

## Program:
```
DEVELOPED BY : GOWTHAM K
REGISTER NUMBER : 26014578

import pandas as pd
url = "https://raw.githubusercontent.com/arunpradeep-sec/Linear-Algebra-Lab/main/carsemission.csv"

df = pd.read_csv(url)
df.to_csv("carsemission.csv", index=False)

print("Dataset loaded successfully.")

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
<img width="1729" height="696" alt="Screenshot (16)" src="https://github.com/user-attachments/assets/63a42056-ee9b-4116-8808-7339027873b0" />




## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
