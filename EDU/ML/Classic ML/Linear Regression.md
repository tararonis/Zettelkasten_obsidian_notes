20:15     2024/01/17    
Tags: #st
____
## Линейная регрессия
> 

Линейная регрессия - это алгоритм вида
![[Pasted image 20240117195043.png]]
где w0..wn - веса, x1..xn - признаки объекта

Веса - параметры модели
Обучение - поиск оптимальных параметров

> Мы изначально предполагаем, что в данных есть линейная зависимость.
> Строим гиперплоскость и предполагаем, что данные/ответы лежат на этой гиперплоскости.

Еще один способ записи:

![[Pasted image 20240117200943.png]]
### В матричном виде
![[Pasted image 20240119194826.png]]

### Обучение линейной регрессии
Суть - минимизация среднеквадратичной ошибки(MSE)
![[Pasted image 20240117201317.png]]
**В матричном виде**
![[Pasted image 20240119194926.png]]
> Обучение любого алгоритма машинного обучения сводится к минимизации какого-то функционала. Чаще всего - это какой-то гладкий дифференцируемый функционал.
>В случае ЛР - функционал ошибки - среднеквадратичное отклонение

> Функционал - это функция, которая принимает на вход другую функцию

> Функция потерь применима к одному объекту, а функционал ошибки - это средняя сумма функций потерь по всей обучающей выборке.

>В такой простой задаче функция выпуклая хоть и находится в многомерном пространстве. Функция имеет один минимум - он и локальный и глобальный.
>Чтобы решить задачу нужно выразить градиент, приравнять его у нулю и выразить веса w. 

### 


____
### Zero-Links
[[Classic ML]]

____
### Links
[[1M. Введение + Линейная регрессия]]