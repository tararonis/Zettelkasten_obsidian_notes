Tags: #
____
![[Pasted image 20240613114213.png]]
>метод регуляризации, служащий предотвращению переобучению.  во время каждой итерации обучения случайно выбранные нейроны исключаются из работы, то есть их выходы устанавливаются в ноль.

>Применение Dropout помогает сети обучаться более устойчиво и предотвращает переобучение, поскольку сеть учится работать с признаками независимо друг от друга, так как часть нейронов может быть "выключена" в любой момент.
![[Pasted image 20240613114240.png]]
> - Dropout борется с явлением co-adaptation - подстройки нейронов друг под друга связанным с этим явлением переобучением.

Модификций drop out очень много:
![[Pasted image 20240613114447.png]]

## **Gaussian Dropout**

Тут мы домножаем выход не на 0 или 1, а на случайную величину из нормального распределения со средним значением 1 и разбросом p(1-p)
То есть влияние нейрона может как уменьшиться, так и увеличиться (в каком-то смысле это обобщение Dropout, который либо оставляет нейрон, либо просто выключает его).


### Code
```python
# Пример архитектуры с Dropout-слоями

class ExampleModel(nn.Module):
    def __init__(self):
        super().__init__()
        self.layer1 = nn.Linear(60, 60)
        self.act1 = nn.ReLU()
        self.dropout1 = nn.Dropout(0.2)
        self.layer2 = nn.Linear(60, 30)
        self.act2 = nn.ReLU()
        self.dropout2 = nn.Dropout(0.2)
        self.output = nn.Linear(30, 1)
        self.sigmoid = nn.Sigmoid()
                                              
    def forward(self, x):
        x = self.act1(self.layer1(x))        
        x = self.dropout1(x)
        x = self.act2(self.layer2(x))
        x = self.dropout2(x)
        x = self.sigmoid(self.output(x))
        return x
```


____
### Zero-Links
[[_DL]]

____
### Links