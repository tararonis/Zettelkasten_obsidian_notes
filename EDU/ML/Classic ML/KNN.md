12:15     2024/02/21    
Tags: #st
____
>_k-nearest neighbors_ - это простой нелинейный алгоритм, применяющийся для решения задач классификации и регрессии.

### Idea
Гипотеза компактности - схожие объекты находятся близко друг к другу в пространстве признаков.

### **Преимущества и недостатки KNN**
#### Pros
- Простой алгоритм (для объяснения и для интерпретации)
- Метод не делает никаких предположений о данных (об их линейной разделимости, о распределении данных)
- В некоторых задачах достаточно хорошо работает
- Применяется и для классификации, и для регрессии
#### Cons
- Требует больших ресурсов по памяти, так как хранит всю выборку
- Требует больших ресурсов по времени, так как вычисляет расстояния до всех объектов выборки
- Чувствителен к масштабу данных
- Зависит от выбранной метрики, которая в свою очередь должна отражать реальное сходство объектов. Найти такую метрику не всегда просто или даже возможно
### **Алгоритм**

У метода есть гиперпараметр к - число соседей.
Чтобы определить, к какому классу относится объект,  нужно:

- вычислить расстояние от объекта до каждого объекта выборки
- выбрать k объектов выборки с наименьшим расстоянием (k ближайших соседей)
- класс искомого объекта - это наиболее часто встречающийся класс среди k ближайших соседей.

![[Pasted image 20240221121828.png]]
### Особенности 
- Метод легко переобучается - при маленьких К разделяющая поверхность очень сложная и подстраивается под данные
- У метода нет фазы обучения
- перед применением обязательно нужно масштабировать

### Метрики
#### Евклидова метрика
![[Pasted image 20240221122147.png]]
![[Pasted image 20240221122204.png]]
#### **Манхеттенское расстояние**
![[Pasted image 20240221122224.png]]
![[Pasted image 20240221122233.png]]

#### **Расстояние Хемминга**
> число различных позиций в координатах двух векторов

![[Pasted image 20240221122314.png]]
#### Мера Жаккара
>  отношение числа совпадающих элементов множеств к общему числу различных элементов.
![[Pasted image 20240221122413.png]]
![[Pasted image 20240221122422.png]]


____
### Zero-Links
[[Classic ML]]

____
### Links
