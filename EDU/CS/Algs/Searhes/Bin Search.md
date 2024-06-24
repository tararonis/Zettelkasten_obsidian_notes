Tags: #
____
## Свойства
Сложность - O(log N)
Худший случай - искомый элемент первый/последний
Лучший - средний элемент - тот который мы ищем

### Pros
- Легкая реализация
- Быстрая работа
## Cons
- Для поиска нужен упорядоченный массив
- Поиск должен иметь возможность обратиться к любому элементу массива, а значит связные списки не подходят.

## Implementation
#### Pseudo Code
```
int binSearch(int[] a, int key):
	int l = -1
	int r = len(a)

	while l< r-1:
		m = l + (r-l) / 2
		if a[m] < key:
			l = m
		else:
			r = m
	return r
```


____
### Zero-Links
[[00 Prog]]

____
### Links
[[1(A). Linear algorithms and Bin Search]]