20:03     2024/01/26    
Tags: #st
____
> хорошее тестовое покрытие - от 80%
### Doctest
0. Тестируем вручную из командной строки
1. Добавляем диалог as is в docstring:
2. Тестирование: python3 -m doctest Moo.py
    
3. Отчёт (с успешными тестами): python3 -m doctest -v Moo.py
    
4. Тестирование исключений
    - Вообще говоря, важны только три строчки (сама команда, первая строка и сообщение с исключением), остальные можно выкинуть
5. [Перенос тестов во внешний текстовый файл](https://docs.python.org/3/library/doctest#simple-usage-checking-examples-in-a-text-file "py3doc"),    
    - например, в .rst        
    - этот файл отлично включается в Sphinx-документацию
    - Запуск python3 exttest.py -v:
```
import doctest
doctest.testfile("exttest.rst")
```
### Mock
[Краткое обоснование Mock на примере]([https://uneex.org/LecturesCMC/PythonDevelopment2021/10_Testing_Mock)




____
### Zero-Links
[[00 Python]]

____
### Links
