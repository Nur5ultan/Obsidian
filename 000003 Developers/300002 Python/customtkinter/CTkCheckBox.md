---
tags: CTk_widgets
---

### Пример кода
```python
def checkbox_event():
    print("checkbox toggled, current value:", check_var.get())

check_var = customtkinter.StringVar(value="on")
checkbox = customtkinter.CTkCheckBox(app, text="CTkCheckBox", command=checkbox_event, variable=check_var, onvalue="on", offvalue="off")
```

### Аргументы
|      Аргументы      |                                        Значение                                         |
|:-------------------:|:---------------------------------------------------------------------------------------:|
|       master        |                            root, tkinter.Фрейм или CTkFrame                             |
|        width        |                             ширина всего виджета в пикселях                             |
|       height        |                             высота всего виджета в пикселях                             |
|   checkbox_width    |                                ширина флажка в пикселях                                 |
|   checkbox_height   |                                высота флажка в пикселях                                 |
|    corner_radius    |                                 радиус угла в пикселях                                  |
|    border_width     |                             ширина границы поля в пикселях                              |
|      fg_color       |     цвет переднего плана (внутри), кортеж: (light_color, dark_color) или один цвет      |
|    border_color     |              цвет границы, кортеж: (light_color, dark_color) или один цвет              |
|     hover_color     |             цвет наведения, кортеж: (light_color, dark_color) или один цвет             |
|     text_color      |              цвет текста, кортеж: (light_color, dark_color) или один цвет               |
| text_color_disabled |      цвет текста, когда отключен, кортеж: (light_color, dark_color) или один цвет       |
|        text         |                                         строка                                          |
|    textvariable     |                        Tkinter StringVar для управления текстом                         |
|        font         |                    шрифт текста кнопки, кортеж: (font_name, размер)                     |
|        hover        |                   включить / отключить эффект наведения: True, False                    |
|        state        | tkinter.ОБЫЧНЫЙ (стандартный) или tkinter.ОТКЛЮЧЕН (не кликабельный, более темный цвет) |
|       command       |                       функция будет вызвана при нажатии на флажок                       |
|      variable       |             Переменная Tkinter для управления состоянием флажка или чтения              |
|       onvalue       |                  строка или int для переменной в проверенном состоянии                  |
|       ffvalue       |                 строка или int для переменной в непроверенном состоянии                 |


### Методы
-  .настроить(атрибут=значение, ...)[](https://customtkinter.tomschimansky.com/documentation/widgets/checkbox#configureattributevalue- "Прямая ссылка на .configure(атрибут=значение, ...)")

Все атрибуты могут быть настроены, например
```python
checkbox.configure(state="disabled")
```

- .cget(имя_атрибута)[](https://customtkinter.tomschimansky.com/documentation/widgets/checkbox#cgetattribute_name "Прямая ссылка на .cget(имя_атрибута)")

Передайте имя атрибута в виде строки и получите, например, текущее значение атрибута.
```python
text = checkbox.cget("text")
```

-  .get()[](https://customtkinter.tomschimansky.com/documentation/widgets/checkbox#get "Прямая ссылка на .get()")
    
    Получаем текущее значение, 1 или 0 (установлено или не установлено).
    
-  .выберите()[](https://customtkinter.tomschimansky.com/documentation/widgets/checkbox#select "Прямая ссылка на .выберите()")
    
    Включите флажок (установите значение равным 1), команда не будет запущена.
    
-  .отмените выбор()[](https://customtkinter.tomschimansky.com/documentation/widgets/checkbox#deselect "Прямая ссылка на .отменить выбор()")
    
    Отключите флажок (установите значение в 0), команда не будет запущена.
    
-  .переключить()[](https://customtkinter.tomschimansky.com/documentation/widgets/checkbox#toggle "Прямая ссылка на .toggle()")
    
    Измените текущее значение, команда будет запущена.

[[виджеты CTk]]
