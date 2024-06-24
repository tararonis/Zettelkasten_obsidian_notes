Tags: #
____
> техника, используемая в глубинном обучении для предотвращения _взрыва градиентов_ во время обучения нейронных сетей. Заключается в ограничении диапазона значений градиентов в заданных пределах. 

> Делается это двумя путями - либо обрезание(значений выше определенного порога)
 либо масштабирования.
 
**Взрыв градиента** - при обратном распространении ошибки, градиент может принимать огромные значения, особенно если у модель много слоев. 
### Вариант процедуры 
![[Pasted image 20240612131957.png]]
### Code
```python
import torch
import torch.nn as nn

# Создаем модель
model = nn.Sequential(
    nn.Linear(10, 5),
    nn.ReLU(),
    nn.Linear(5, 1)
)

# Определяем функцию потерь
criterion = nn.MSELoss()

# Задаем оптимизатор
optimizer = torch.optim.SGD(model.parameters(), lr=0.01)

# Задаем параметры gradient clipping
max_grad_norm = 1.0  # Максимальная допустимая норма градиентов
clip_type = 'norm'  # Может быть 'norm' или 'value'

# Пример обучения с gradient clipping
inputs = torch.randn(1, 10)
targets = torch.randn(1, 1)

# Прямой проход
outputs = model(inputs)
loss = criterion(outputs, targets)

# Обратное распространение ошибки
optimizer.zero_grad()
loss.backward()

# Применение gradient clipping
if clip_type == 'norm':
    torch.nn.utils.clip_grad_norm_(model.parameters(), max_grad_norm)
elif clip_type == 'value':
    torch.nn.utils.clip_grad_value_(model.parameters(), max_grad_norm)

# Обновление весов
optimizer.step()
```

____
### Zero-Links
[[_DL]]

____
### Links