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

### How to insert column on selected index
``` 
df['new_col'] = …
df.insert(2, "new column", df.pop("new_col"))
```

____
### Zero-Links
[[00 Prog]] [[00 ML]]
____
### Links