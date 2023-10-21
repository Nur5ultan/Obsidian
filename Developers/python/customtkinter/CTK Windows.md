---
tags: customtkinter
---

Класс CTk составляет основу любой программы CustomTkinter, он создает главное окно приложения. Во время выполнения программы должен существовать только один экземпляр этого класса с единственным вызовом `.mainloop()` метода, который запускает приложение. Дополнительные окна создаются с использованием класса CTkToplevel.

### Пример кода
Пример без использования классов:
```python
app = customtkinter.CTk()
app.geometry("600x500")
app.title("CTk example")

app.mainloop()
```

Пример с классами:
```python
class App(customtkinter.CTk):
    def __init__(self):
        super().__init__()
        self.geometry("600x500")
        self.title("CTk example")

        # add widgets to app
        self.button = customtkinter.CTkButton(self, command=self.button_click)
        self.button.grid(row=0, column=0, padx=20, pady=10)

    # add methods to app
    def button_click(self):
        print("button click")


app = App()
app.mainloop()
```

### Аргументы
| Аргумент | Значение                                                        |
| -------- | --------------------------------------------------------------- |
| fg_color | цвет фона окна, кортеж: (light_color, dark_color) или один цвет |

### Methods[](https://customtkinter.tomschimansky.com/documentation/windows/window#methods "Direct link to Methods")

- #### .configure(attribute=value, ...)[](https://customtkinter.tomschimansky.com/documentation/windows/window#configureattributevalue- "Direct link to .configure(attribute=value, ...)")
    
    Все атрибуты могут быть настроены и обновлены, например:
```python
app.configure(fg_color=new_fg_color)
```

#### .cget(attribute_name)[](https://customtkinter.tomschimansky.com/documentation/windows/window#cgetattribute_name "Direct link to .cget(attribute_name)")

Передайте имя атрибута в виде строки и получите текущее значение атрибута, например:
```python
fg_color = app.cget("fg_color")
```

- #### .title(string)[](https://customtkinter.tomschimansky.com/documentation/windows/window#titlestring "Direct link to .title(string)")
    
    Задайте заголовок окна.
    
- #### .geometry(geometry_string)[​](https://customtkinter.tomschimansky.com/documentation/windows/window#geometrygeometry_string "Direct link to .geometry(geometry_string)")
    
    Установите минимальный размер окна.: `"<width>x<height>"` или `"<width>x<height>+<x_pos>+<y_pos>"`
    
- #### .minsize(width, height)[​](https://customtkinter.tomschimansky.com/documentation/windows/window#minsizewidth-height "Direct link to .minsize(width, height)")
    
    Set minimal window size.
    
- #### .maxsize(width, height)[​](https://customtkinter.tomschimansky.com/documentation/windows/window#maxsizewidth-height "Direct link to .maxsize(width, height)")
    
    Установите максимальный размер окна.
    
- #### .resizable(width, height)[​](https://customtkinter.tomschimansky.com/documentation/windows/window#resizablewidth-height "Direct link to .resizable(width, height)")
    
  Определите, следует ли изменять ширину и / или высоту с помощью значений bool.
    
- #### .after(milliseconds, command)[​](https://customtkinter.tomschimansky.com/documentation/windows/window#aftermilliseconds-command "Direct link to .after(milliseconds, command)")
    
    Выполнить команду через миллисекунды, не блокируя основной цикл.
    
- #### .withdraw()[​](https://customtkinter.tomschimansky.com/documentation/windows/window#withdraw "Direct link to .withdraw()")
    
    Скрыть окно и значок. Восстановите его с помощью .deiconify().
    
- #### .iconify()[​](https://customtkinter.tomschimansky.com/documentation/windows/window#iconify "Direct link to .iconify()")
    
   Отображает окно. Восстановите его с помощью .deiconify().
    
- #### .deiconify()[​](https://customtkinter.tomschimansky.com/documentation/windows/window#deiconify "Direct link to .deiconify()")
    
    Деиконифицируйте окно.
    
- #### .state(new_state)[​](https://customtkinter.tomschimansky.com/documentation/windows/window#statenew_state "Direct link to .state(new_state)")
    
    Устанавливает состояние окна ('обычное', 'знаковое', 'удаленное', 'увеличенное'), возвращает текущее состояние, если аргумент не передан.

[[Python/customtkinter]]