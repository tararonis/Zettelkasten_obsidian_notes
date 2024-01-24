20:41     2024/01/19    
Tags: #st 
____
### Split data
```
from sklearn.model_selection import train_test_split

Xtrain, Xtest, ytrain, ytest = train_test_split(X, y, test_size=0.3, random_state=42)

```

## Preprocessing
### [StandardScaler](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.StandardScaler.html)
> Standardize features by removing the mean and scaling to unit variance
> >The standard score of a sample `x` is calculated as:
> >z = (x - u) / s
> >where `u` is the mean of the training samples or zero if `with_mean=False`, and `s` is the standard deviation of the training samples or one if `with_std=False`.

```
from sklearn.preprocessing import StandardScaler  

scaler=StandardScaler()  
# train scaler on train data
scaler.fit(Xtrain)

Xtrain_scaled = scaler.transform(Xtrain)
# as the result we have numpy array so conversion 2 pd is required
Xtrain_scaled = pd.DataFrame(Xtrain_scaled, columns=Xtrain.columns)  
# or just write Xtrain_scaled = scaler.fit_transform(Xtrain)

Xtest_scaled = scaler.transform(Xtest)
Xtest_scaled = pd.DataFrame(Xtest_scaled, columns=Xtest.columns)
```

### [PolynomialFeatures](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.PolynomialFeatures.html#sklearn.preprocessing.PolynomialFeatures)

```
from sklearn.preprocessing import PolynomialFeatures  

pf = PolynomialFeatures(degree = 2)

pf.fit(Xtrain)
Xtrain = pf.transform(Xtrain)
```


## Metrics
### [R2 score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.r2_score.html#sklearn.metrics.r2_score)

description -> [[R2 score]]

```
from sklearn.metrics import r2_score

print(r2_score(ytrain, linreg.predict(Xtrain_scaled)))
print(r2_score(ytest, linreg.predict(Xtest_scaled)))

```
### MSE
```
from sklearn.metrics import mean_squared_error
mse = mean_squared_error(y_true, y_pred)
```
## Models
### [LinearRegression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html#sklearn.linear_model.LinearRegression)

description -> [[Linear Regression]]
```
from sklearn.linear_model import LinearRegression
  

linreg = LinearRegression()
linreg.fit(Xtrain_scaled, ytrain)
linreg.predict(Xtrain_scaled)

print(r2_score(ytest, linreg.predict(Xtest_scaled)))
```

## Регуляризация
### Ridge
```
from sklearn.linear_model import Ridge
model_l2 = Ridge(alpha=1)
model_l2.fit(Xtrain, ytrain)
pred_l2 = model_l2.predict(Xtest)
```
### Lasso
```
from sklearn.linear_model import Lasso 

model_l1 = Lasso(alpha=3.5)
model_l1.fit(Xtrain, ytrain)
pred_l1 = model_l1.predict(Xtest)
```
### L1+L2 (ElasticNet)
```
from sklearn.linear_model import ElasticNet  

model_l2 = ElasticNet(alpha=0.5, l1_ratio=0)
model_l2.fit(Xtrain, ytrain)
pred_l2 = model_l2.predict(Xtest)
____
### Zero-Links
[[00 ML]][[00 Prog]]
____
### Links