Tags: #
____
![[Pasted image 20240614165234.png]]
>это полносвязная нейронная сеть с одним скрытым слоем.
## Idea
> _**слова, встречающиеся в похожих контекстах, имеют близкие друг к другу векторы**

## Algorithm
- На вход сети подаются слова контекста, закодированные при помощи OneHot-кодирования 
- На выходе мы получаем вектор размерности количества слов в словаре, где на i-й позиции стоит вероятность того, что внутри данного контекста стоит i-е слово из словаря
![[Pasted image 20240614170325.png]]
PS:
	- на скрытом слое нет функции активации
	- на выходном - softmax
	- функция потерь: cross-entropy loss(log-loss)
	  ![[Pasted image 20240614170513.png]]
### Как получаем вектор слова
![[Pasted image 20240614170643.png]]
> это i строка матрицы W'

 Еще варианты:
- взять матрицу W
- посчитать среднее по W and W' 
## Мера близости слов
> _**косинусная близость**_

![[Pasted image 20240614171027.png]]
____
### Zero-Links
[[_NLP]]

____
### Links