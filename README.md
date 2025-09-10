# Predicting-Paychecks-with-Machine-Learning-in-Python
Predict employee paychecks using data preprocessing, feature engineering and supervised ML (Linear Regression, Random Forest, XGBoost) with examples and a Streamlit demo.
import pandas as pd

url = "https://archive.ics.uci.edu/ml/machine-learning-databases/adult/adult.data"
cols = [
    'age','workclass','fnlwgt','education','education_num','marital_status',
    'occupation','relationship','race','sex','capital_gain','capital_loss',
    'hours_per_week','native_country','income'
]

data = pd.read_csv(url, names=cols, sep=r',\s*', engine='python', header=None)
data.to_csv("data/adult.csv", index=False)
