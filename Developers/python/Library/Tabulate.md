---
tags: cli, lib_py
---

```python
from tabulate import tabulate  
  
data = [  
["Apple", 1.2, 7],  
["Banana", 0.9, 5],  
["Cherry", 1.5, 3]  
]  
  
headers = ["Fruit", "Price", "Quantity"]  
  
print(tabulate(data, headers=headers, tablefmt="grid"))
```

Библиотека Tabulate предназначена для красивого вывода табличных данных. Она поддерживает различные форматы таблиц и позволяет легко выводить данные в виде таблицы с заголовками и разделителями.

Основные возможности библиотеки Tabulate:
- Вывод табличных данных в различных форматах (plain, simple, grid, pipe, orgtbl, tsv, html, latex, ts, и др.).
- Автоматическое определение заголовков таблицы.
- Поддержка разных типов данных (числа, строки, списки, кортежи, словари и др.).

В результате работы кода из примера выводится таблица с данными о фруктах, их цене и количестве, оформленная в формате "grid".
