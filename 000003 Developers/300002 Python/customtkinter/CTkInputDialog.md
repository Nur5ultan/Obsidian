---
tags: customtkinter
---

Это простое диалоговое окно для ввода строки или числа.

### Пример кода
```python
dialog = customtkinter.CTkInputDialog(text="Type in a number:", title="Test")
text = dialog.get_input()  # waits for input
```

Пример внутри программы:
```python
app = customtkinter.CTk()
app.geometry("400x300")


def button_click_event():
    dialog = customtkinter.CTkInputDialog(text="Type in a number:", title="Test")
    print("Number:", dialog.get_input())


button = customtkinter.CTkButton(app, text="Open Dialog", command=button_click_event)
button.pack(padx=20, pady=20)

app.mainloop()
```

Результатом этого примера является следующее окно и диалоговое окно:
![[Pasted image 20230629233627.png]]



 

### Аргументы[](https://customtkinter.tomschimansky.com/documentation/windows/inputdialog#arguments "Прямая ссылка на аргументы")

|аргумент|значение|
|---|---|
|Название|строка для заголовка диалогового окна|
|текст|текст для самого диалогового окна|
|fg_color|цвет окна, кортеж: (light_color, dark_color) или один цвет|
|button_fg_color|цвет кнопок, кортеж: (light_color, dark_color) или один цвет|
|button_hover_color|цвет кнопок при наведении курсора мыши, кортеж: (light_color, dark_color) или один цвет|
|button_text_color|цвет текста кнопок, кортеж: (light_color, dark_color) или один цвет|
|entry_fg_color|цвет ввода, кортеж: (light_color, dark_color) или один цвет|
|цвет_бордера_ входа|цвет границы записи, кортеж: (light_color, dark_color) или один цвет|
|entry_text_color|цвет текста для ввода, кортеж: (light_color, dark_color) или один цвет|

### Методы[](https://customtkinter.tomschimansky.com/documentation/windows/inputdialog#methods "Прямая ссылка на методы")

- #### .get_input()[](https://customtkinter.tomschimansky.com/documentation/windows/inputdialog#get_input "Прямая ссылка на .get_input()")
    
    Возвращает ввод, ожидает нажатия кнопки "Ок" или "Отмена".

[[Python/customtkinter]]




