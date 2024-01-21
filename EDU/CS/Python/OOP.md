17:12     2024/01/21    
Tags: #st
____
## dataclass
чтобы не мучиться  с прописанием _init_, repr и прочей дичью можно использовать декоратор
@dataclass from lib dataclasses
```
from dataclasses import dataclass 

@dataclass
class Point: 
	x: float
	y: float 
	label: str
```


____
### Zero-Links
[[00 Python]]
____
### Links
Немного доки:
- [dataclasses](https://docs.python.org/3/library/dataclasses.html)
- [guide](https://realpython.com/python-data-classes/)