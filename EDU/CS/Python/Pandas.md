19:45     2024/01/19    
Tags: #st 
____
### Показать описание по категориальным признакам
```data.describe(include='object')```
### Удалить колонку
```data.drop('Unnamed: 0', axis=1, inplace=True)```

### [One-hot](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.get_dummies.html)
```
pd.get_dummies(data, drop_first=True)
pd.get_dummies(data, drop_first=True, columns=['column_nameA'])
```
### Show n random objects
``` df.sample(n)```

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
```
____
### Zero-Links
[[00 Prog]] [[00 ML]]
____
### Links