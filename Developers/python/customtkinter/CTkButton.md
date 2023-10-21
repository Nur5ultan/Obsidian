---
tags: CTk_widgets
---

### Пример кода
```python
def button_event():
    print("button pressed")

button = customtkinter.CTkButton(app, text="CTkButton", command=button_event)
```

### Аргументы
|      Аргументы           |            Значение             |
|:---------------------:|:-------------------------------:|
|       master                  | root, tkinter.Frame or CTkFrame |
|        width                   |    ширина кнопки в пикселях     |
|       height                   |    высота кнопки в пикселях     |
|    corner_radius          |     радиус угла в пикселях      |
|    border_width           |             ширина границы кнопки в пикселях |
|   border_spacing        |  интервал между текстом и изображением и границей кнопки в пикселях, по умолчанию равен 2 |
|      fg_color                | для основного цвета, кортеж: (light_color, dark_color) или одноцветный, или "прозрачный" |
|     hover_color           | цвет наведения, кортеж: (light_color, dark_color) или один цвет |
|    border_color          | цвет границы, кортеж: (light_color, dark_color) или один цвет |
|     text_color             | цвет текста, кортеж: (light_color, dark_color) или один цвет |
| text_color_disabled | цвет текста, когда отключен, кортеж: (light_color, dark_color) или один цвет |
|        text                   |  строка |
|        font                   |  шрифт текста кнопки, кортеж: (font_name, size), (установите отрицательное значение размера для размера в пикселях) |
|    textvariable           |  tkinter.StringVar object to change text of button |
|        image                | помещаем изображение на кнопку, удаляем текст, должен быть класс PhotoImage |
|        state                  | "обычный" (стандартный) или "отключенный" (не кликабельный, более темный цвет) |
|        hover                 |  включить / отключить эффект наведения: True, False |
|       command            | функция обратного вызова |
|      compound            | установите ориентацию изображения, если заданы изображение и текст ("сверху", "слева", "снизу", "справа") |
|       anchor                 |  выравнивание текста и изображения в кнопке ("n", "ne", "e", "se", "s", "sw", "w", "nw", "center") |

### Методы
-  .configure(attribute=value, ...)
Все атрибуты могут быть настроены, например:
```python
button.configure(text="new text")
```

-  .cget(attribute_name)
Передайте имя атрибута в виде строки и получите, например, текущее значение атрибута.
```python
text = button.cget("text")
```

-  .invoke()
Вызывает команду, если состояние кнопки "отключено".

[[Developers/python/customtkinter/виджеты CTk]]
