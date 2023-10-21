---
tags: customtkinter
---

### Базовое приложение
Прежде всего, убедитесь, что у вас установлена последняя версия CustomTkinter. Затем вы можете протестировать свою установку с помощью самой простой программы, которая создает только окно:

```python
import customtkinter

app = customtkinter.CTk()
app.mainloop()
```

Если это работает, вы можете начать настраивать свойства окна, такие как `title` и `geometry`, и начать добавлять кнопку в окно. Первым параметром любого виджета всегда является главный параметр, который `app`в данном случае. Он также может быть задан с ключевым аргументом (`master=app`).

```python
import customtkinter

def button_callback():
    print("button pressed")

app = customtkinter.CTk()
app.title("my app")
app.geometry("400x150")

button = customtkinter.CTkButton(app, text="my button", command=button_callback)
button.grid(row=0, column=0, padx=20, pady=20)

app.mainloop()
```

### Менеджер геометрии сетки
В этом примере `grid` менеджер геометрии используется для установки положения и заполнения виджета. Настоятельно рекомендуется всегда использовать `grid`geometry Manager вместо `place` и `pack`, потому что с его помощью очень легко создавать адаптивные и расширяемые пользовательские интерфейсы.

`grid` Разбивает окно или рамку на столбцы и строки, которые сворачиваются, когда они пусты, но адаптируются к размеру виджетов, размещенных внутри них. Если вы хотите расположить кнопку по центру в последнем примере, вам придется присвоить первому столбцу вес, отличный от нуля, чтобы он больше не уменьшался до размера кнопки (используйте `grid_rowconfigure()` для строк):

```python
app.grid_columnconfigure(0, weight=1)
```

Теперь столбец 0 занимает все окно, потому что он имеет вес 1 и, следовательно, расширяется. Вы также можете настроить кнопку так, чтобы она расширялась вместе с ячейкой сетки, если вы добавите `sticky` аргумент к `grid` вызову следующим образом:

```python
button.grid(row=0, column=0, padx=20, pady=20, sticky="ew")
```

Теперь кнопка прилипает к ячейке сетки с восточной и западной сторон. Вы можете заметить, что ячейка сетки и, следовательно, размер кнопки меняются при изменении размера окна.

### Добавьте флажки

```python
checkbox_1 = customtkinter.CTkCheckBox(app, text="checkbox 1")
checkbox_1.grid(row=1, column=0, padx=20, pady=(0, 20), sticky="w")
checkbox_2 = customtkinter.CTkCheckBox(app, text="checkbox 2")
checkbox_2.grid(row=1, column=1, padx=20, pady=(0, 20), sticky="w")
```

Обратите внимание, что `pady` аргумент получает кортеж, который означает 0 отступов сверху и 20 отступов снизу. Также обратите внимание, что флажки прикреплены только к западной стороне соответствующей ячейки сетки. Чтобы кнопка снова охватывала все окно, нам нужно установить для нее значение, `columnspan` равное 2 (используйте `rowspan` для строк).

```python
button.grid(row=0, column=0, padx=20, pady=20, sticky="ew", columnspan=2)
```

И чтобы равномерно расставить флажки, нам также нужно придать обоим столбцам одинаковый вес.

```python
app.grid_columnconfigure((0, 1), weight=1)
```

Теперь полная программа выглядит следующим образом:

```python
def button_callback():
    print("button pressed")

app = customtkinter.CTk()
app.title("my app")
app.geometry("400x150")
app.grid_columnconfigure((0), weight=1)

button = customtkinter.CTkButton(app, text="my button", command=button_callback)
button.grid(row=0, column=0, padx=20, pady=20, sticky="ew", columnspan=2)
checkbox_1 = customtkinter.CTkCheckBox(app, text="checkbox 1")
checkbox_1.grid(row=1, column=0, padx=20, pady=(0, 20), sticky="w")
checkbox_2 = customtkinter.CTkCheckBox(app, text="checkbox 2")
checkbox_2.grid(row=1, column=1, padx=20, pady=(0, 20), sticky="w")

app.mainloop()
```

### Использование классов
Чтобы завершить это введение, мы хотим структурировать эту программу в класс. Настоятельно рекомендуется использовать классы, которые наследуются от `CTk`, для главного окна или `CTkFrame` фрейма, потому что это значительно повышает читаемость кода, и код становится легко расширяемым, поскольку классы могут быть легко распределены по нескольким файлам.

```danger
- [f] ОСТОРОЖНО
За исключением небольших программ или тестов, всегда создавайте отдельные классы для `CTk`, `CTkToplevel` или `CTkFrame`. Писать много кода пользовательского интерфейса в одном файле без использования классов - это боль для чтения и очень плохой стиль кодирования.
```

```python
class App(customtkinter.CTk):
    def __init__(self):
        super().__init__()

        self.title("my app")
        self.geometry("400x150")
        self.grid_columnconfigure((0, 1), weight=1)

        self.button = customtkinter.CTkButton(self, text="my button", command=self.button_callback)
        self.button.grid(row=0, column=0, padx=20, pady=20, sticky="ew", columnspan=2)
        self.checkbox_1 = customtkinter.CTkCheckBox(self, text="checkbox 1")
        self.checkbox_1.grid(row=1, column=0, padx=20, pady=(0, 20), sticky="w")
        self.checkbox_2 = customtkinter.CTkCheckBox(self, text="checkbox 2")
        self.checkbox_2.grid(row=1, column=1, padx=20, pady=(0, 20), sticky="w")
        
    def button_callback(self):
        print("button pressed")

app = App()
app.mainloop()
```

[[Python/customtkinter]]
