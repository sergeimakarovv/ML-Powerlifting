# ML Powerlifting

### **Description:**

The project is focused on predicting the best deadlift weight an ahtlete can lift. It includes training different machine learning models, comparing their performance, and applying data cleaning and dimensionality reduction techniques.

[![dataset-cover.png](https://i.postimg.cc/Pr6n5tpf/dataset-cover.png)](https://postimg.cc/qzC5mHxW)

The dataset was downloaded from [**Kaggle**](https://www.kaggle.com/datasets/open-powerlifting/powerlifting-database/data?select=openpowerlifting-2024-01-06-4c732975.csv). 

It contains data about the athletes' characteristics, lifted weights on different attempts, powerlifting indices, and information about the sport events.

### **Python libraries used:** 

- scikit-learn: ML models, evaluation metrics and dimensionality reduction
- pandas: data cleaning and processing
- seaborn, plotly: creating visualizations

## **Project overview**

**1. Data cleaning and transformation**

Only some part of the data is selected for better model fit, redundant and missing data is deleted. Initial model predictors are chosen: *Sex, Age, Bodyweight, Best3SquatKg, Best3BenchKg*. Cathegorical data is transformed into numeric with one-hot encoding. 

**2. Variance Inflation Factor (VIF) Analysis**

The VIF analysis is applied to tackle multicollinearity between the predictors. The dependent variables are transformed and combined. 

**3. Linear Regression and Cross-validation**

The data is scaled and splitted into training and testing sets. The Linear Regression model is trained and evaluated by several metrics: *median absolute error, mean absolute error, mean squared error, root mean squared error, coefficient of determination*. Cross-validation with different K-fold scores is applied (K-fold = 3, 5, 10).   

**4. Principal Component Analysis (PCA)**

PCA is implemented to reduce the data dimensionality and to try improving the model performance. 

**5. Other types of regressions**

Finally, other types of regression are trained and evaluated: *Polynomial Regression, Ridge Regression, Random Forest Regression*. 

## **Notes**

In order to run the code, ensure to download the necessary packages as in `requirements.txt` and download the dataset `openpowerlifting-2024-01-06-4c732975.csv` from Kaggle.
