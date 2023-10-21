---
tags: gui
---
## Installation

> [!Note] PyPI Installation
> python -m pip install ttkbootstrap

>[!Note] Github Installation
>python -m pip install git+https://github.com/israel-dryer/ttkbootstrap



```python
# Импортируем библиотеку ttkbootstrap и назначаем ей сокращение tb для дальнейшего использования
import ttkbootstrap as tb  

# Создаём окно программы и назначаем ей тему "darkly"
app = tb.Window(themename="darkly")  
# Задаем размеры окна
app.geometry("400x400")
# Задаем заголовок
app.title("res editor with ttkbootsrap")


first_entry = tb.Entry(app) # создаём поле ввода
first_entry.grid(row=1, column=0)  # размещаем поле вводу на главном окне
  
app.mainloop() # не даём программе сразу закрыться

```


[[!gui]]
